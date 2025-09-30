.. _PhysiCell_java_CancerImmune_CancerInstantiator_java:

CancerInstantiator.java
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

    import ru.biosoft.physicell.core.Cell;
    import ru.biosoft.physicell.core.CellDefinition;
    import ru.biosoft.physicell.core.CellFunctions.Instantiator;
    import ru.biosoft.physicell.core.Model;
    import ru.biosoft.physicell.core.SignalBehavior;
    import ru.biosoft.physicell.biofvm.Microenvironment;

    public class CancerInstantiator extends Instantiator
    {
        @Override
        public Cell execute(CellDefinition cd, Model model) throws Exception
        {
            Cell cell = new Cell( cd, model );
            cell.parameters.o2_proliferation_saturation = 38.0;
            cell.parameters.o2_reference = 38.0;
            cell.phenotype.mechanics.relMaxAttachmentDistance = cd.custom_data.get( "max_attachment_distance" ) / cd.phenotype.geometry.radius;
            cell.phenotype.mechanics.relDetachmentDistance = cd.custom_data.get( "max_attachment_distance" ) / cd.phenotype.geometry.radius;
            cell.phenotype.mechanics.attachmentElasticConstant = cd.custom_data.get( "elastic_coefficient" );
            return cell;
        }

    }