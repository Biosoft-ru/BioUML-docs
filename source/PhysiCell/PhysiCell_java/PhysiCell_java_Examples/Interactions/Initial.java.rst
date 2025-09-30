.. _PhysiCell_java_Interactions_Initial_java:

Initial.java
============

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

    import ru.biosoft.physicell.core.Model;
    import ru.biosoft.physicell.core.PhysiCellUtilities;
    import ru.biosoft.physicell.core.InitialCellsArranger;

    public class Initial extends InitialCellsArranger
    {      
        @Override
        public void arrange(Model model) throws Exception
        {
            PhysiCellUtilities.place( model, "bacteria", model.getParameterInt( "number_of_bacteria" ) );
            PhysiCellUtilities.place( model, "blood vessel", model.getParameterInt( "number_of_blood_vessels" ) );
            PhysiCellUtilities.place( model, "stem", model.getParameterInt( "number_of_stem_cells" ) );
            PhysiCellUtilities.place( model, "differentiated", model.getParameterInt( "number_of_differentiated_cells" ) );
            PhysiCellUtilities.place( model, "macrophage", model.getParameterInt( "number_of_macrophages" ) );
            PhysiCellUtilities.place( model, "neutrophil", model.getParameterInt( "number_of_neutrophils" ) );
            PhysiCellUtilities.place( model, "CD8+ T cell", model.getParameterInt( "number_of_CD8T_cells" ) );
        }
    }