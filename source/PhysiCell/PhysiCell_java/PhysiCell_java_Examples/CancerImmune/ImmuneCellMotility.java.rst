.. _PhysiCell_java_CancerImmune_ImmuneCellMotility_java:

ImmuneCellMotility.java
=======================

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

    import ru.biosoft.physicell.biofvm.Microenvironment;
    import ru.biosoft.physicell.biofvm.VectorUtil;
    import ru.biosoft.physicell.core.Cell;
    import ru.biosoft.physicell.core.CellFunctions.UpdateMigrationBias;
    import ru.biosoft.physicell.core.Phenotype;

    /**
    * If not attached move towards immunostimulatory factor, otherwise do not move
    */
    public class ImmuneCellMotility extends UpdateMigrationBias
    {
        @Override
        public void execute(Cell pCell, Phenotype phenotype, double dt)
        {
            Microenvironment m = pCell.getMicroenvironment();
            int immuneFactorIndex = m.findDensityIndex( "immunostimulatory factor" );
            if( pCell.state.attachedCells.size() == 0 )
            {
                phenotype.motility.isMotile = true;
                phenotype.motility.migrationBiasDirection = VectorUtil.newNormalize( pCell.nearest_gradient( immuneFactorIndex ) );
            }
            else
            {
                phenotype.motility.isMotile = false;
            }
        }

        @Override
        public String display()
        {
            return "If not attached move towards immunostimulatory factor, otherwise do not move";
        }
    }