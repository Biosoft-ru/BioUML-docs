.. _PhysiCell_java_PredatorPreyFarmer_WeightedMotility_java:

WeightedMotility.java
=====================

.. role:: raw-html(raw)
   :format: html

.. raw:: html

   <style>
   pre {
      white-space: pre-wrap !important;       /* Сохраняет пробелы, но разрешает перенос */
      word-wrap: break-word !important;       /* Переносит длинные слова */
      overflow-wrap: break-word !important;   /* Альтернатива для совместимости */
      hyphens: auto !important;               /* Перенос с тире */
   }
   </style>

.. code-block:: console

    import ru.biosoft.physicell.biofvm.VectorUtil;
    import ru.biosoft.physicell.core.Cell;
    import ru.biosoft.physicell.core.CellFunctions.UpdateMigrationBias;
    import ru.biosoft.physicell.core.Phenotype;

    /**
    * Motility based on substrate gradients with specified weights
    */
    public class WeightedMotility extends UpdateMigrationBias
    {
        @Override
        public void execute(Cell pCell, Phenotype phenotype, double dt)
        {
            weightedMotility( pCell, phenotype, dt );
        }

        public static void weightedMotility(Cell pCell, Phenotype phenotype, double dt)
        {
            double[] direction = phenotype.motility.migrationBiasDirection;
            VectorUtil.zero( direction );
            VectorUtil.axpy( direction, pCell.customData.get( "prey_weight" ), pCell.nearestGradient( "prey signal" ) );
            VectorUtil.axpy( direction, pCell.customData.get( "predator_weight" ), pCell.nearestGradient( "predator signal" ) );
            VectorUtil.axpy( direction, pCell.customData.get( "food_weight" ), pCell.nearestGradient( "food" ) );
            VectorUtil.normalize( direction );
        }

        @Override
        public String display()
        {
            return "Motility based on substrate gradients with specified weights.";
        }
    }