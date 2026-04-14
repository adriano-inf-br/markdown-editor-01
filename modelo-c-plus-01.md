#include <iostream>
#include <vector>

int main() {
    std::vector<int> pedidos = {12, 18, 25, 30};
    int soma = 0;

    for (int quantidade : pedidos) {
        soma += quantidade;
    }

    std::cout << "Itens processados: " << soma << std::endl;
    return 0;
}
