/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package mx.unam.aragon.fes;

/**
 *
 * @author Charli
 */
public class Empleado extends Persona{

    private int numeroEpleado;
    private String departamento;
    private Float sueldo; 
    private int horasExtra;
    private Direccion domicilio;

    public Empleado() {
    }

    public Empleado(int numeroEpleado, String departamento, Float sueldo, int horasExtra, Direccion domicilio) {
        this.numeroEpleado = numeroEpleado;
        this.departamento = departamento;
        this.sueldo = sueldo;
        this.horasExtra = horasExtra;
        this.domicilio = domicilio;
    }

    public Empleado(int numeroEpleado, String departamento, Float sueldo, int horasExtra, Direccion domicilio, String nombre, String apPaterno, String apMaterno, int edad, String curp) {
        super(nombre, apPaterno, apMaterno, edad, curp);
        this.numeroEpleado = numeroEpleado;
        this.departamento = departamento;
        this.sueldo = sueldo;
        this.horasExtra = horasExtra;
        this.domicilio = domicilio;
    }

    public int getNumeroEpleado() {
        return numeroEpleado;
    }

    public void setNumeroEpleado(int numeroEpleado) {
        this.numeroEpleado = numeroEpleado;
    }

    public String getDepartamento() {
        return departamento;
    }

    public void setDepartamento(String departamento) {
        this.departamento = departamento;
    }

    public Float getSueldo() {
        return sueldo;
    }

    public void setSueldo(Float sueldo) {
        this.sueldo = sueldo;
    }

    public int getHorasExtra() {
        return horasExtra;
    }

    public void setHorasExtra(int horasExtra) {
        this.horasExtra = horasExtra;
    }

    public Direccion getDomicilio() {
        return domicilio;
    }

    public void setDomicilio(Direccion domicilio) {
        this.domicilio = domicilio;
    }

    public float calcularSueldo(){
        //Horas extra a $150.00
        float sueldoTotal = 0.0f;
        sueldoTotal = this.sueldo + (this.horasExtra * 150.0f);
                
        return sueldoTotal;
    }

    @Override
    public String toString() {
        return "Empleado{" + "numeroEpleado=" + numeroEpleado + "\n departamento=" + departamento + "\n sueldo=" + sueldo + "\n horasExtra=" + horasExtra + "\n domicilio=" + domicilio + '}';
    }
    
    
    
}
