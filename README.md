# funciones-en-c-
Crear dos funciones , 1 que rellene el array del main y otra que calcule la medai de las temperaturas de los paises
using System;

namespace Prueba9
{
    class Program
    {
        static void Main(string[] args)
        {
            //cramos el array que alamcenará el listado de paises y sus temperaturas
            string[] listado = new string[5];

            //llamamos a la funcion RellenarListado para que rellene el array listado
            RellenarListado(listado);

            //muestra el contenido introducido en la funcion RellenarListado
            foreach (string i in listado)
            {
                Console.WriteLine("El pais y su temperatura: " + i);
            }

            //Llamamos la funcion CalcularMedia
            int media = CalcularMedia(listado);





            Console.ReadLine();

        }

        //Creamos la funcion para que rellene el array
        static string[] RellenarListado(string[] listado)
        {


            for (int i = 0; i < listado.Length; i++)
            {
                Console.WriteLine("introduce el pais y su temperatura: ");
                listado[i] = Console.ReadLine();
            }

            return listado;

        }

        //Creamos la funcion para que calcule la media de los paises.
        static int CalcularMedia(string[] listado)
        {

            int temperatura = 0;


            

            foreach (string valor in listado)
            {

                string[] valor_separado = valor.Split(",");

                

                temperatura += int.Parse(valor_separado[1]);

                Console.WriteLine(valor_separado[1]);
                
            }

           temperatura /= listado.Length;
            return temperatura;

        }
    }
}
