.. _PhysiCell_java_CancerImmune_AdhesionContact_java:

AdhesionContact.java
====================

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
    import ru.biosoft.physicell.core.CellFunctions.Contact;
    import ru.biosoft.physicell.core.Phenotype;

    public class AdhesionContact extends Contact
    {
        public void execute(Cell pActingOn, Phenotype pao, Cell pAttachedTo, Phenotype pat, double dt)
        {
            double[] displacement = VectorUtil.newDiff( pAttachedTo.position, pActingOn.position );
            double maxElasticDisplacement = pao.geometry.radius * pao.mechanics.relDetachmentDistance;
            double maxDisplacementSquared = maxElasticDisplacement * maxElasticDisplacement;

            // detach cells if too far apart 
            if( VectorUtil.norm_squared( displacement ) > maxDisplacementSquared )
            {
                Cell.detachCells( pActingOn, pAttachedTo );
                return;
            }
            VectorUtil.axpy( pActingOn.velocity, pao.mechanics.attachmentElasticConstant, displacement );
        }
    }