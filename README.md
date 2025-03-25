1 ejercicio

#include <iostream>

int main() {
    int num1, num2, suma;

    std::cout << "Ingrese el primer número: ";
    std::cin >> num1;

    std::cout << "Ingrese el segundo número: ";
    std::cin >> num2;

    suma = num1 + num2;

   
    std::cout << "La suma es: " << suma << std::endl;

    return 0;
}

2. Resta de dos números  
Crea un programa que permita al usuario ingresar dos 
números y calcule la diferencia entre ellos. en c++


#include <iostream>

int main() {
    int num1, num2, diferencia;

    std::cout << "Ingrese el primer número: ";
    std::cin >> num1;
    std::cout << "Ingrese el segundo número: ";
    std::cin >> num2;
    diferencia = num1 - num2;

    std::cout << "La diferencia entre " << num1 << " y " << num2 << " es: " << diferencia << std::endl;

    return 0;
}

3. Producto de dos números  
Escribe un programa que multiplique dos números dados por el usuario.

#include <iostream>

int main() {
    double num1, num2, producto;

    
    std::cout << "Ingrese el primer número: ";
    std::cin >> num1;
    std::cout << "Ingrese el segundo número: ";
    std::cin >> num2;

    producto = num1 * num2;

    std::cout << "El producto es: " << producto << std::endl;

    return 0;
}

4. División de dos números  
Pide al usuario que ingrese dos números y calcule su división. 
Asegúrate de manejar la entrada para que el divisor no sea 0. 


#include <iostream>
#include <limits> 

int main() {
    double dividendo, divisor, resultado;

    
    std::cout << "Ingrese el dividendo: ";
    std::cin >> dividendo;
    std::cout << "Ingrese el divisor: ";
    std::cin >> divisor;

    if (divisor == 0) {
        std::cout << "Error: No se puede dividir por cero." << std::endl;
    } else {
        
        resultado = dividendo / divisor;
        std::cout << "La división de " << dividendo << " entre " << divisor << " es: " << resultado << std::endl;
    }
    
    if (std::cin.fail()) {
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        std::cout << "Error: Entrada inválida." << std::endl;
    }

    return 0;
}


#include <iostream>
#include <limits> 

int main() {
    
    int num1_residuo, num2_residuo, residuo;

    std::cout << "Ejercicio 5: Residuo (módulo) entre dos números" << std::endl;
    std::cout << "Ingrese el primer número entero: ";
    std::cin >> num1_residuo;

   
    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el primer número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        return 1; 
    }

    std::cout << "Ingrese el segundo número entero (no cero): ";
    std::cin >> num2_residuo;

   
    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el segundo número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        
        return 1; 
    if (num2_residuo == 0) {
        std::cout << "Error: El segundo número no puede ser cero para el módulo." << std::endl;
    } else {
        residuo = num1_residuo % num2_residuo;
        std::cout << "El residuo de " << num1_residuo << " entre " << num2_residuo << " es: " << residuo << std::endl;
    }
    std::cout << std::endl;
    

    // 6. Calcular promedio de tres números


    double num1_promedio, num2_promedio, num3_promedio, promedio;

    std::cout << "Ejercicio 6: Calcular promedio de tres números" << std::endl;
    std::cout << "Ingrese el primer número: ";
    std::cin >> num1_promedio;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el primer número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        return 1;
    }

    std::cout << "Ingrese el segundo número: ";
    std::cin >> num2_promedio;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el segundo número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        return 1;
    }

    std::cout << "Ingrese el tercer número: ";
    std::cin >> num3_promedio;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el tercer número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        return 1;
    }

    promedio = (num1_promedio + num2_promedio + num3_promedio) / 3.0;
    std::cout << "El promedio de " << num1_promedio << ", " << num2_promedio << " y " << num3_promedio << " es: " << promedio << std::endl;

    return 0;
}

#include <iostream>
#include <limits> 

int main() {


    // 7. Invertir un número de dos cifras


    int numero_invertir;

    std::cout << "Ejercicio 7: Invertir un número de dos cifras" << std::endl;
    std::cout << "Ingrese un número de dos cifras (entre 10 y 99): ";
    std::cin >> numero_invertir;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else if (numero_invertir >= 10 && numero_invertir <= 99) {
        int decena = numero_invertir / 10;
        int unidad = numero_invertir % 10;
        int invertido = (unidad * 10) + decena;
        std::cout << "El número invertido es: " << invertido << std::endl;
    } else {
        std::cout << "Error: El número ingresado no es de dos cifras." << std::endl;
    }
    std::cout << std::endl;

    // 8. Área de un rectángulo

    double base_rectangulo, altura_rectangulo, area_rectangulo;

    std::cout << "Ejercicio 8: Área de un rectángulo" << std::endl;
    std::cout << "Ingrese la base del rectángulo: ";
    std::cin >> base_rectangulo;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para la base." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else {
        std::cout << "Ingrese la altura del rectángulo: ";
        std::cin >> altura_rectangulo;

        if (std::cin.fail()) {
            std::cout << "Error: Entrada inválida para la altura." << std::endl;
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        } else {
            area_rectangulo = base_rectangulo * altura_rectangulo;
            std::cout << "El área del rectángulo es: " << area_rectangulo << std::endl;
        }
    }
    std::cout << std::endl;

    // 9. Comparación de dos números

    int num1_comparacion, num2_comparacion;
    std::cout << "Ejercicio 9: Comparación de dos números" << std::endl;
    std::cout << "Ingrese el primer número: ";
    std::cin >> num1_comparacion;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el primer número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else {
        std::cout << "Ingrese el segundo número: ";
        std::cin >> num2_comparacion;

        if (std::cin.fail()) {
            std::cout << "Error: Entrada inválida para el segundo número." << std::endl;
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        } else {
            if (num1_comparacion == num2_comparacion) {
                std::cout << "Ambos números son iguales." << std::endl;
            } else {
                std::cout << "Los números son diferentes." << std::endl;
            }
        }
    }
    std::cout << std::endl;

    // 10. Suma y producto de dos números

    double num1_syP, num2_syP, suma_syP, producto_syP;
    std::cout << "Ejercicio 10: Suma y producto de dos números" << std::endl;
    std::cout << "Ingrese el primer número: ";
    std::cin >> num1_syP;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida para el primer número." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else {
        std::cout << "Ingrese el segundo número: ";
        std::cin >> num2_syP;

        if (std::cin.fail()) {
            std::cout << "Error: Entrada inválida para el segundo número." << std::endl;
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        } else {
            suma_syP = num1_syP + num2_syP;
            producto_syP = num1_syP * num2_syP;
            std::cout << "La suma es: " << suma_syP << std::endl;
            std::cout << "El producto es: " << producto_syP << std::endl;
        }
    }

    return 0;
}

segunda parte de ejercicios

#include <iostream>
#include <string>
#include <limits> 
#include <cctype> 


int main() {
    
    
    // 1. Verificar números pares en un rango
    
    
    int inicio_rango, fin_rango;
    std::cout << "Ejercicio 1: Verificar números pares en un rango" << std::endl;
    std::cout << "Ingrese el número de inicio del rango: ";
    std::cin >> inicio_rango;
    std::cout << "Ingrese el número de fin del rango: ";
    std::cin >> fin_rango;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else {
        std::cout << "Números pares en el rango [" << inicio_rango << ", " << fin_rango << "]:" << std::endl;
        if (inicio_rango > fin_rango) {
            std::swap(inicio_rango, fin_rango); 
        }
        for (int i = inicio_rango; i <= fin_rango; ++i) {
            if (i % 2 == 0) {
                std::cout << i << " ";
            }
        }
        std::cout << std::endl << std::endl;
    }

    // 2. Calcular la suma de números positivos
    
    int numero_positivo;
    int suma_positivos = 0;
    std::cout << "Ejercicio 2: Calcular la suma de números positivos" << std::endl;
    std::cout << "Ingrese una serie de números (ingrese un número no positivo para terminar):" << std::endl;
    while (true) {
        std::cout << "Ingrese un número: ";
        std::cin >> numero_positivo;
        if (std::cin.fail()) {
            std::cout << "Error: Entrada inválida." << std::endl;
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
            break;
        }
        if (numero_positivo <= 0) {
            break;
        }
        suma_positivos += numero_positivo;
    }
    std::cout << "La suma de los números positivos ingresados es: " << suma_positivos << std::endl << std::endl;

    // 3. Encontrar el número mayor
    
    
    int num_mayor;
    int numero_actual;
    std::cout << "Ejercicio 3: Encontrar el número mayor" << std::endl;
    std::cout << "Ingrese cinco números:" << std::endl;
    for (int i = 0; i < 5; ++i) {
        std::cout << "Ingrese el número " << i + 1 << ": ";
        std::cin >> numero_actual;
        if (std::cin.fail()) {
            std::cout << "Error: Entrada inválida." << std::endl;
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
            return 1; 
        }
        if (i == 0 || numero_actual > num_mayor) {
            num_mayor = numero_actual;
        }
    }
    std::cout << "El número mayor ingresado es: " << num_mayor << std::endl << std::endl;

    // 4. Tablas de multiplicar
    
    
    int num_tabla;
    std::cout << "Ejercicio 4: Tablas de multiplicar" << std::endl;
    std::cout << "Ingrese un número para ver su tabla de multiplicar: ";
    std::cin >> num_tabla;

    if (std::cin.fail()) {
        std::cout << "Error: Entrada inválida." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else {
        std::cout << "Tabla de multiplicar del " << num_tabla << ":" << std::endl;
        for (int i = 1; i <= 10; ++i) {
            std::cout << num_tabla << " x " << i << " = " << (num_tabla * i) << std::endl;
        }
        std::cout << std::endl;
    }

    // 5. Contar vocales en una cadena
    
    
    std::string cadena;
    int contador_vocales = 0;
    std::cout << "Ejercicio 5: Contar vocales en una cadena" << std::endl;
    std::cout << "Ingrese una cadena de texto: ";
    std::cin.ignore(); 
    std::getline(std::cin, cadena);

    for (char c : cadena) {
        char letra = std::tolower(c); 
        if (letra == 'a' || letra == 'e' || letra == 'i' || letra == 'o' || letra == 'u') {
            contador_vocales++;
        }
    }
    std::cout << "La cadena ingresada tiene " << contador_vocales << " vocales." << std::endl << std::endl;

    // 6. Calcular el factorial (módulo 10)
    
    
    int numero_factorial;
    long long factorial = 1; 
    std::cout << "Ejercicio 6: Calcular el factorial (módulo 10)" << std::endl;
    std::cout << "Ingrese un número entero positivo: ";
    std::cin >> numero_factorial;

    if (std::cin.fail() || numero_factorial < 0) {
        std::cout << "Error: Entrada inválida. Ingrese un entero positivo." << std::endl;
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
    } else {
        for (int i = 1; i <= numero_factorial; ++i) {
            factorial *= i;
        }
        std::cout << "El factorial de " << numero_factorial << " es: " << factorial << std::endl;
        std::cout << "El factorial de " << numero_factorial << " módulo 10 es: " << factorial % 10 << std::endl;
    }

    return 0;
}
