/**
* FILE:		1CV10	Práctica 2 en C++
*     Programación estructurada – parte 1
*
*
* DESCRIPCION:
* Uso de tipos de datos numéricos,
*  operadores aritméticos y funciones estándares de
*  flujo de entrada/salida en
*  lenguaje de programación C y C++
* 
* nota : este programa lo hice en "online GDB" 
* 
* AUTOR:   Fungus	🍄 
* FECHA:		Oct 15 , 2023
*
**/
#include <iostream>
#include <iomanip>
#include <cmath>
using namespace std;

double fahrenheitACelsius(double fahrenheit) {
    return (fahrenheit - 32) * 5.0 / 9.0; }
int main() {

    // 1.1. Imprimir entero 40000 justificado a la izquierda en un campo de 15 digitos
    cout << "1.1. 🍄  → " << left << setw(15) << 40000 << endl;
    cout << " " << endl;
    
    // 1.2. Leer una cadena en el arreglo de caracteres estado
    char estado[100]; // Se reserva espacio para almacenar la cadena
    std::cout << "1.2. 🍄  → Por favor, ingresa el estado: ";
    std::cin >> std::setw(99) >> estado; // Se utiliza setw para evitar desbordamientos
    std::cout << "El estado ingresado es: " << estado << std::endl;
    cout << " " << endl;
    // 1.3. Imprimir 200 con y sin signo
    int num1 = 200;
    std::cout << "1.3. 🍄  → Imprimir 200 con y sin signo: " << num1 << " " << std::showpos << num1 << std::noshowpos << std::endl;
cout << " " << endl;
    // 1.4. Imprimir valor decimal 100 en formato hexadecimal precedido por 0x
    int num2 = 100;
    std::cout << " 1.4. 🍄  → El valor en formato hexadecimal de 100 es: 0x" << std::hex << num2 << std::dec << std::endl;
   cout << " " << endl;
	// 1.5. Imprimir 1.234 en un campo de 9 digitos con ceros a la izquierda
   std::cout<<"1.5 🍄  → Imprima en consola 1.234 en un campo de 9 digitos con ceros a la izquierda:"<<endl;
    cout<< setiosflags(ios::internal);
    cout<< setw(10) << setfill('0') <<1.234<<endl;
cout << " " << endl;
    // 1.6. Evaluar entrada de xvalores enteros en formato decimal, octal y hexadecimal
int valor;
    cout << "1.6.🍄 → Por favor, ingresa un valor en formato decimal, octal o hexadecimal: ";
    cin >> valor;

    cout << "Valor en decimal: \t" << valor << endl;
    cout << "Valor en octal: \t" << oct << valor << endl;
    cout << "Valor en hexadecimal: \t" << hex << valor << endl;
cout << " " << endl;
    // 1.7. Despliegue en consola tres caracteres leidos por el programa en los tres formatos: decimal, octal y hexadecimal
   char char1, char2, char3;
    std::cout << "1.7. 🍄 Por favor, ingresa tres caracteres separados por espacios: ";
    std::cin >> char1 >> char2 >> char3;
    
    std::cout << "Caracteres en decimal: " << int(char1) << " " << int(char2) << " " << int(char3) << std::endl;
    std::cout << "Caracteres en octal: " << std::oct << int(char1) << " " << int(char2) << " " << int(char3) << std::dec << std::endl;
    std::cout << "Caracteres en hexadecimal: " << std::hex << int(char1) << " " << int(char2) << " " << int(char3) << std::dec << std::endl;
cout << " " << endl;
    // 1.8. Imprima el valor 100.453627 redondeado al digito mÃ¡s cercano, dÃ©cimas, centÃ©simas, milÃ©simas y diezmilÃ©simas.
   cout << "1.8.🍄  → " <<  "Redondeado al dígito más cercano: " << (100.453627) << endl;
    cout << "Redondeado a decimas: " << fixed << setprecision(1) << 100.453627 << endl;
    cout << "Redondeado a centesimas: " << fixed << setprecision(2) << 100.453627 << endl;
    cout << "Redondeado a milésimas: " << fixed << setprecision(3) << 100.453627 << endl;
    cout << "Redondeado a diezmilésimas: " << fixed << setprecision(4) << 100.453627 << endl;

cout << " " << endl;
    // 1.9. Convierta temperaturas enteras en Fahrenheit desde 0 a 212 grados, a temperaturas Celsius en punto flotante con 3 digitos de precisiÃ³n.
cout <<"\n" << "1.9.🍄  temperaturas de 0 a 212 Fahrenheit a Celsius ↓ \n "  << "-----------------------------------\n";
cout << std::setw(12) << "Fahrenheit  |  Celsius   |  \n";
    cout << "-----------------------------------\n";
    for (int fahrenheit = 0; fahrenheit <= 212; ++fahrenheit) {
        double celsius = fahrenheitACelsius(fahrenheit);
        cout << setw(1) << fahrenheit << "           |  " << showpos << fixed << setprecision(3) << celsius << "   | " << noshowpos << endl;
    }
    return 0;
}
