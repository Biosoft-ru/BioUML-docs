.. _PhysiCell_java_ODEEnergy_ODEVisualizer_java:

ODEVisualizer.java
==================

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

    import java.awt.Color;

    import ru.biosoft.physicell.core.Cell;
    import ru.biosoft.physicell.ui.FalseCellCytometryVisualizer;

    public class ODEVisualizer extends FalseCellCytometryVisualizer
    {
        @Override
        public Color[] findColors(Cell pCell)
        {
            try
            {
            double energy = pCell.phenotype.intracellular.getParameterValue( "$Intracellular.Energy" );
            Color[] output = super.findColors( pCell );
            if( pCell.type == 0 )
            {
                // dead cell
                if( pCell.phenotype.death.dead )
                {
                    output[0] = new Color( 20, 20, 20 );
                    output[2] = new Color( 10, 10, 10 );
                }
                else  if( energy <= 445 )
                {
                    output[0] = new Color( 255, 0, 0 );
                    output[2] = new Color( 125, 0, 0 );
                }
                else
                {
                    output[0] = new Color( 255, 255, 0 );
                    output[2] = new Color( 125, 125, 0 );
                }
            }
            return output;
        }
        catch (Exception ex)
        {
                return new Color[]{new Color(255, 0, 0)};
        }
        }
    }