# Exercicios-01_04
Exercicios de 01 ao 04



01-
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

/*Faça um algoritmo que leia a idade de uma pessoa expressa em anos, meses e dias e escreva
 a idade dessa pessoa expressa apenas em dias.Considerar ano com 365 dias e mês com 30 dias.*/

namespace Calcular_Idade
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello!");

            const int ano = 365;
            int mes = 30;
            int dia = 12;

            Console.Write("Informe seu dia de nascimento: ");
            int dianascimento = int.Parse(Console.ReadLine());

            Console.Write("Informe seu mês de nascimento: ");
            int mesnascimento = int.Parse(Console.ReadLine());

            Console.Write("Informe seu ano de nascimento: ");
            int anonascimento = int.Parse(Console.ReadLine());


            Console.Write("Informe o dia atual: ");
            int mesatual = int.Parse(Console.ReadLine());

            Console.Write("Informe seu mês de atual: ");
            int diaatual = int.Parse(Console.ReadLine());

            Console.Write("Informe o ano atual: ");
            int anoatual = int.Parse(Console.ReadLine());


            Console.WriteLine("Você nasceu em : " + dianascimento + "/" + mesnascimento + "/" + anonascimento);


            int mesdia = ((mes - mesnascimento) * dia) + (dia - dianascimento);
            int idade = (anoatual - 1) - anonascimento;
            int idadedia = (idade * ano) + mesdia;
            int diasmes = (dia * mesatual) + (dia - diaatual);
            int result = idadedia + diasmes;

            Console.WriteLine("Sua idade é:" + idade + "anos");


            Console.WriteLine("Você viveu :" + result + "dias");

            Console.ReadKey();
        }
    }
}
------------------------------------------------------------------------------------------

02-

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

/* Escreva um algoritmo para ler o número total de eleitores de um município, o número de
votos brancos, nulos e válidos.Calcular e escrever o percentual que cada um representa em
relação ao total de eleitores.*/

namespace calcular_numero_eleitores
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello!");

            Console.WriteLine("Informe a quantidade de eleitores:");
            double eleitores = double.Parse(Console.ReadLine());

            Console.WriteLine("Informe quantidade de votos branco:");
            double brancos = double.Parse(Console.ReadLine());

            Console.WriteLine("Informe quantidade de votos nulos:");
            double nulos = double.Parse(Console.ReadLine());

            double porbranco = (brancos * 100) / eleitores;
            double porcnulo = (nulos * 100) / eleitores;
            double porcvalido = eleitores - (brancos + nulos);


            Console.WriteLine("\nVotos Branco:" + porbranco + "%");
            Console.WriteLine("\nVotos Nulos:" + porcnulo + "%");
            Console.WriteLine("\nVotos validos:" + porcvalido * 100 / eleitores + "%");

            Console.WriteLine();

        }
    }
}
------------------------------------------------------------------------------------------

03-

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


/*O custo de um carro novo ao consumidor é a soma do custo de fábrica com a porcentagem
do distribuidor e dos impostos(aplicados ao custo de fábrica). Supondo que o percentual do
distribuidor seja de 28% e os impostos de 45%, escrever um algoritmo para ler o custo de
fábrica de um carro, calcular e escrever o custo final ao consumidor.*/

namespace Custo_carro_fabrica
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello!");


            Double custoConsumidor;
            Double porcentagemDistribuidor = 28.0;
            Double PercentualImpostos = 45.0;
            Double Destribuidor;
            Double ValorImpostos;


            Console.WriteLine("Informe o custo de fábrica de um carro novo");
            double custoFabrica = double.Parse(Console.ReadLine());


            ValorImpostos = (custoFabrica * PercentualImpostos) / 100;

            Destribuidor = (custoFabrica * porcentagemDistribuidor) / 100;

            custoConsumidor = (Destribuidor + ValorImpostos + custoFabrica);

            Console.WriteLine("Valor dos Impostos: " + ValorImpostos);
            Console.WriteLine("Valor do Destribuidor: " + Destribuidor);
            Console.WriteLine("Custo de Fabrica: " + custoFabrica);

            Console.WriteLine("O custo ao consumidor de um carro novo é: " + custoConsumidor);

            Console.ReadKey();
        
        }
    }
}
----------------------------------------------------------------------------------------

04-

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

/*Ler 3 valores (considere que não serão informados valores iguais)e escrever o maior deles.*/

namespace Maior_Valor
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Informe 3 valores diferentes: ");

            Console.WriteLine("Informe o primeiro valor: ");
            int primeiro = int.Parse(Console.ReadLine());

           
           Console.WriteLine("Informe o segundo valor : ");
           int segundo = int.Parse(Console.ReadLine());

            while (segundo == primeiro)
            {
                Console.WriteLine("Informe um valor diferente: ");
                int segundo1 = int.Parse(Console.ReadLine());
               segundo = segundo1;
            }

            Console.WriteLine("Informe o terceiro valor : ");
            int terceiro = int.Parse(Console.ReadLine());

            while ((terceiro == primeiro)||(terceiro == segundo))
            {
                Console.WriteLine("Informe um valor diferente: ");
                int terceiro1 = int.Parse(Console.ReadLine());
                terceiro = terceiro1;
            }

            if ((segundo > primeiro)&&(segundo > terceiro))
            {
                Console.WriteLine("O maior valor é " + segundo);
            }
            else if ((terceiro > primeiro) && (terceiro > segundo))
            {

                Console.WriteLine("O maior valor é " + terceiro);
            }
            else
            {
                Console.WriteLine("O maior valor é " + primeiro);
            }

            

            //Aguarda uma tecla a ser precionada
            Console.ReadKey();
        }
    }
}
