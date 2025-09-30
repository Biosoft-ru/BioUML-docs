.. _PhysiCell_java_PredatorPreyFarmer_PPFReport_java:

PPFReport.java
==============

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

    import ru.biosoft.physicell.core.ReportGenerator;
    import ru.biosoft.physicell.core.Cell;

    public class PPFReport extends ReportGenerator
    {
        public String[] getReportHeaderElements()
        {
            return new String[] {"ID", "X", "Y", "Z", "Cycle", "Elapsed"};
        }

        public Object[] getReportElements(Cell cell) throws Exception
        {
            return new Object[] {cell.ID, cell.position[0], cell.position[1], cell.position[2], cell.phenotype.cycle.currentPhase().name,
                    cell.phenotype.cycle.data.elapsedTimePhase};
        }
    }