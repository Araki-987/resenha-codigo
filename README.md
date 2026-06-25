# resenha-codigo

engulo uma garrafa de alcool e me sinto como um Godzilla , é melhor acertarem o convés como o Godzilla , e a minha equipe inteira está aqui andando pela festa , uma mistura de zumbi com um bolso do Zimbabue  , com a chuva aquecendo , o que explica o porque de eu lutar com os barbeadores da mania nessa merda , a 5 minutos atrás , eu tomei um puta esporro do meu chefe na frente de todos os meus colegas de de trabalho  , e a minha namorada terminou comigo , que vida legal ein 

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
