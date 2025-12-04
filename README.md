# poo-Electrodomesticos
Profe no pude conectar mi trabajo para subirlo por lo que voyh a pasar el codigo que hice por aca
package co.edu.poli.electrodomesticos;

/**
 *
 * @author USER
 */
public class Television extends Electrodomesticos{
    
    private double resolucion;
    private boolean sintonizadorTDT;
    
    private static final double RESOLUCION_DEF = 20;
    private static final boolean SINTONIZADOR_TDT_DEF = false;

    public Television() {
        super();
        this.resolucion = RESOLUCION_DEF;
        this.sintonizadorTDT = SINTONIZADOR_TDT_DEF;
    }
    

    public Television(double precioBase, double peso) {
        super(precioBase, peso);
        this.resolucion = RESOLUCION_DEF;
        this.sintonizadorTDT = SINTONIZADOR_TDT_DEF;
    }

    public Television(double precioBase, double peso, char consumoEnergetico, String color, double resolucion, boolean sintonizadorTDT) {
        super(precioBase, peso, consumoEnergetico, color);
        this.resolucion = resolucion;
        this.sintonizadorTDT = sintonizadorTDT;
    }


    public double getResolucion() {
        return resolucion;
    }

    public boolean isSintonizadorTDT() {
        return sintonizadorTDT;
    }


    @Override
    public double precioFinal() {
        double precio = super.precioFinal();

        if (resolucion > 40) {
            precio *= 1.30;
        }


        if (sintonizadorTDT) {
            precio += 50;
        }

        return precio;
    }
}

