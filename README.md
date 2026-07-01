# resenha-codigo

engulo uma garrafa de alcool e me sinto como um Godzilla , a 5 minutos atrás , eu tomei um puta esporro do meu chefe na frente de todos os meus colegas de de trabalho  , e a minha namorada terminou comigo , que legal ein 

#include <iostream>
#include <string>
#include <thread>
#include <chrono>
#include<locale>
using namespace std;

int main() {
set_locale(ALL_"Portuguese")
    string letra[] = {
    
        //coloque aqui a letra da musica que quiser 
        
    };

    int totalLinhas = sizeof(letra) / sizeof(letra[0]);

    for (int i = 0; i < totalLinhas; i++) {
        cout << letra[i] << endl;
        this_thread::sleep_for(chrono::seconds(2)); // Aguarda 2 segundos entre as linhas
    }

    return 0;
}






ABAIXO UM CÓDIGO DE UMA CALCULADORA CIENTÍCA :3

#include <iostream>
#include <iomanip>
#include <cmath>
#include <limits>

using namespace std;

// Constante PI
const double PI = 3.14159265358979323846;

// Função para calcular fatorial
long long fatorial(int n)
{
    long long fat = 1;

    for (int i = 2; i <= n; i++)
        fat *= i;

    return fat;
}

// Função para validar entrada numérica
template <typename T>
bool lerNumero(T &valor)
{
    cin >> valor;

    if (cin.fail())
    {
        cin.clear();
        cin.ignore(numeric_limits<streamsize>::max(), '\n');
        return false;
    }

    return true;
}

int main()
{
    cout << fixed << setprecision(6);

    int opcao;
    double a, b;

    do
    {
        cout << "\n=========================================\n";
        cout << "      CALCULADORA CIENTIFICA C++\n";
        cout << "=========================================\n";
        cout << " 1  - Soma\n";
        cout << " 2  - Subtracao\n";
        cout << " 3  - Multiplicacao\n";
        cout << " 4  - Divisao\n";
        cout << " 5  - Potencia (x^y)\n";
        cout << " 6  - Raiz Quadrada\n";
        cout << " 7  - Seno\n";
        cout << " 8  - Cosseno\n";
        cout << " 9  - Tangente\n";
        cout << "10  - Logaritmo (base 10)\n";
        cout << "11  - Logaritmo Natural (ln)\n";
        cout << "12  - Fatorial\n";
        cout << "13  - Porcentagem\n";
        cout << "14  - Valor Absoluto\n";
        cout << "15  - Raiz Cubica\n";
        cout << "16  - Potencia ao Quadrado\n";
        cout << "17  - Potencia ao Cubo\n";
        cout << "18  - Resto da Divisao\n";
        cout << " 0  - Sair\n";
        cout << "=========================================\n";

        cout << "Escolha uma opcao: ";

        if (!lerNumero(opcao))
        {
            cout << "Entrada invalida!\n";
            continue;
        }

        switch (opcao)
        {
    case 1:
{
    cout << "Entrou no case 1\n";

    double x, y;

    cout << "Primeiro numero: ";
    cin >> x;

    cout << "Segundo numero: ";
    cin >> y;

    cout << "Resultado = " << x + y << endl;

    system("pause");
    break;
}

        case 2:
            cout << "Digite dois numeros: ";

            if (lerNumero(a) && lerNumero(b))
                cout << "Resultado = " << a - b << endl;
            else
                cout << "Entrada invalida.\n";

            break;

        case 3:
            cout << "Digite dois numeros: ";

            if (lerNumero(a) && lerNumero(b))
                cout << "Resultado = " << a * b << endl;
            else
                cout << "Entrada invalida.\n";

            break;

        case 4:
            cout << "Digite dois numeros: ";

            if (!(lerNumero(a) && lerNumero(b)))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            if (b == 0)
                cout << "Erro! Divisao por zero.\n";
            else
                cout << "Resultado = " << a / b << endl;

            break;

        case 5:
            cout << "Base: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Expoente: ";

            if (!lerNumero(b))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << pow(a, b) << endl;
            break;

        case 6:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            if (a < 0)
                cout << "Nao existe raiz real.\n";
            else
                cout << "Resultado = " << sqrt(a) << endl;

            break;

        case 7:
            cout << "Angulo em graus: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << sin(a * PI / 180.0) << endl;
            break;

        case 8:
            cout << "Angulo em graus: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << cos(a * PI / 180.0) << endl;
            break;

        case 9:
        {
            cout << "Angulo em graus: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            double rad = a * PI / 180.0;

            if (fabs(cos(rad)) < 1e-10)
                cout << "Tangente indefinida para este angulo.\n";
            else
                cout << "Resultado = " << tan(rad) << endl;

            break;
        }
              case 10:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            if (a <= 0)
                cout << "Logaritmo invalido.\n";
            else
                cout << "Resultado = " << log10(a) << endl;

            break;

        case 11:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            if (a <= 0)
                cout << "Logaritmo invalido.\n";
            else
                cout << "Resultado = " << log(a) << endl;

            break;

        case 12:
        {
            int n;

            cout << "Digite um numero inteiro: ";

            if (!lerNumero(n))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            if (n < 0)
                cout << "Nao existe fatorial negativo.\n";
            else if (n > 20)
                cout << "Numero muito grande para long long.\n";
            else
                cout << "Resultado = " << fatorial(n) << endl;

            break;
        }

        case 13:
            cout << "Digite o valor: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Digite a porcentagem: ";

            if (!lerNumero(b))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << (a * b) / 100 << endl;
            break;

        case 14:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << fabs(a) << endl;
            break;

        case 15:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << cbrt(a) << endl;
            break;

        case 16:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << pow(a, 2) << endl;
            break;

        case 17:
            cout << "Digite um numero: ";

            if (!lerNumero(a))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            cout << "Resultado = " << pow(a, 3) << endl;
            break;

        case 18:
            cout << "Digite dois numeros: ";

            if (!(lerNumero(a) && lerNumero(b)))
            {
                cout << "Entrada invalida.\n";
                break;
            }

            if (b == 0)
                cout << "Erro! Divisao por zero.\n";
            else
                cout << "Resultado = " << fmod(a, b) << endl;

            break;

        case 0:
            cout << "\nObrigado por utilizar a calculadora!\n";
            break;

        default:
            cout << "Opcao invalida!\n";
            break;
        }

    } while (opcao != 0);

    return 0;
}
    } while(opcao != 0);

    return 0;
}
