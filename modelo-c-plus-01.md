#include <iostream>
#include <vector>
#include <string>

int main() {
    std::vector<std::string> status = {"pendente", "separacao", "enviado"};

    for (const auto& item : status) {
        std::cout << "Status monitorado: " << item << std::endl;
    }

    return 0;
}
