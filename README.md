# Ejercicio Programación Orientada a objetos con Java

### 

### Este ejercicio está diseñado para poner en práctica los conceptos básicos de la programación orientada a objetos, se sugiere leer todos los pasos antes de comenzar a escribir cualquier línea de código.

## Parte 1

#### 1. Revisa y descarga todas las clases del código de este repositorio, puedes importarlo al IDE de tu preferencia.

#### 2. Ejecuta la clase `SimulaBanco`  y analiza el resultado y el porqué del mismo.

#### 3.  Existe una clase abstracta llamada `Cuenta` de la cual se deben heredar dos clases `CuentaDebito` y `CuentaCredito`.

 ![Cuenta](https://raw.githubusercontent.com/jcgeneration/CH25_JavaPOO/main/Cuenta.jpg)



![Diagrama Clases](https://raw.githubusercontent.com/jcgeneration/CH25_JavaPOO/main/DiagramaClasesPaquete.png)





#### 4. `CuentaDebito` debe implementar la siguiente propiedad y métodos:

a) Propiedad `montoMinimo` que debe ser el monto mínimo en promedio que debe tener la cuenta para no cobrar por el manejo de cuenta.

b) Get y Set de la propiedad `montoMinimo`.

c) Método `getSaldo` que regresa el saldo de la cuenta.

d) Método `retiro` donde se evalúe si el saldo es suficiente para poder realizar el retiro  y actualizar el saldo, finalmente debe regresar el saldo de la cuenta.

e) Método `deposito`  donde se actualiza el saldo de la cuenta y finalmente debe regresar el saldo de la cuenta.

f) Método toString que llame al método de la clase `Cuenta` de la siguiente manera:

```java
public String toString() {
		return "Cuenta Débito [" + super.toString() + 
				", Monto mínimo=" + montoMinimo + "]";
	}//toString
```

#### 5. `CuentaCredito` debe implementar las siguientes propiedades y métodos:

a) `limite` que es el límite de crédito con el que se cuenta.

b) `tasa` que es la tasa de interés que se cobra si no se paga .

c) `fechaCorte` que es la fecha de corte de la cuenta de crédito.

d) `fechaLimitePago` que es la fecha que se tiene para pagar antes de cobrar intereses.

e) Getters y Setters de las propiedades `tasa`, `limite`, `fechaCorte`.

f) Método `getSaldo` que regresa el saldo de la cuenta y cobra una comisión de $$ 3 pesos por cada solicitud de saldo (esta comisión se ve reflejada en el saldo actual).

g) Método `retiro` donde se evalúe si el límite menos el saldo actual es suficiente para poder realizar el retiro, de no ser así debe cobrarse una comisión de $$5, si se puede realizar el retiro se aumenta al saldo y se cobra una comisión del 5 % (del total del retiro)  y en los dos casos actualiza el saldo, finalmente debe regresar el saldo de la cuenta.

h) Método `deposito` donde se actualiza el saldo de la cuenta y finalmente debe regresar el saldo de la cuenta.

i) Método toString que llame al método de la clase `Cuenta` de la siguiente manera:

```java
	public String toString() {
		return "Cuenta Crédito [" + super.toString() +
				" Tasa=" + getTasa() + "%, Límite="
				+ getLimite() + "]";
	}//toString

```

#### 6. Ejecuta nuevamente y ve el resultado

#### 7. Realiza 4 operaciones sobre las cuentas existentes, retiros y depósitos, previo a imprimir los saldos.

## 

## Parte 2

### Se necesita crear una clase `TarjetaRegalo` y hacer que la clase ReciboSaldo pueda imprimir el saldo de este tipo de cuenta con el mismo método `Imprimir`.

#### 1. Crear la clase `TarjetaRegalo` de acuerdo al siguiente diagrama:



![Tarjeta Regalo](https://raw.githubusercontent.com/jcgeneration/CH25_JavaPOO/main/TarjetaRegalo.png)



#### 2. Crear la interfaz `Imprimible` que defina los métodos `getNumeroCuenta` y `getSaldo`.

#### 3. Implementa la interfaz `Imprimible` en `CuentaDebito`, `CuentaCredito` y `TarjetaRegalo`.

#### 4. Dentro de la clase `ReciboSaldo` cambia el tipo de dato del método `Imprimir` por `Imprimible`.

#### 5. Crea un objeto del tipo `TarjetaRegalo` en el `main` de la clase `SimulaBanco` e imprime el saldo mediante la clase `ReciboSaldo`.

### 

## Parte 3 (Opcional)

#### Crear una clase que represente al banco (`Banco`) que permita administrar diferentes tipos de cuentas mediante métodos para agregar, acceder , modificar y cancelar cuentas.

#### Debe tener la posibilidad de generar un reporte que muestre cuanto dinero tiene el banco en todas sus cuentas de débito, y a cuanto asciende la deuda de todas las cuentas de crédito. Así como un reporte donde imprima el  resumen de todas las cuentas.
