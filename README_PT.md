# FheTranspilerCpp

**Nota:** A estrutura de compilação FHE de próxima geração, **[HEIR](https://github.com/google/heir)**, sucedeu este repositório. Recomendamos fortemente a visita ao [repositório GitHub do HEIR](https://github.com/google/heir) e ao seu site oficial [https://heir.dev](https://heir.dev) para os avanços mais recentes.

## Visão Geral

**FheTranspilerCpp** (anteriormente "fully-homomorphic-encryption") é uma biblioteca e cadeia de ferramentas de código aberto projetada para fechar o gap entre o desenvolvimento padrão em C++ e a Encriptação Homomórfica Total (FHE). Ele funciona como um compilador que converte a lógica padrão de C++ em código C++ compatível com FHE, capaz de operar sobre conjuntos de dados encriptados.

### O que é Encriptação Homomórfica Total (FHE)?

A Encriptação Homomórfica Total é uma técnica criptográfica de ponta que permite a realização de operações matemáticas em dados encriptados sem a necessidade de descriptografá-los primeiro. Isso cria uma mudança de paradigma onde a privacidade dos dados e o processamento de dados podem coexistir perfeitamente.

**O Problema:** Tradicionalmente, se um aplicativo precisava processar dados encriptados, ele tinha que:
1. Descriptografar os dados.
2. Realizar o cálculo.
3. Reencriptar os resultados.
Isso expõe dados sensíveis à camada de aplicação.

**A Solução:** O FHE introduz uma transformação de cálculo `F'` que pode ser aplicada diretamente aos dados encriptados. O resultado é a encriptação da saída desejada: `F(dados_desencriptados) = Descriptografar(F'(dados_encriptados))`.

### O Transpiler C++ para FHE

Este projeto fornece um transpiler de propósito geral com uma arquitetura modular. Ele permite que pesquisadores e desenvolvedores:

*   **Troquem Bibliotecas FHE:** Escolha o backend criptográfico subjacente.
*   **Definam Lógica de Alto Nível:** Descreva programas em C++ padrão.
*   **Alvo de Saídas Específicas:** Gere código FHE-C++ otimizado.

Ao automatizar a tradução de lógica para circuitos compatíveis com FHE, esta ferramenta minimiza a sobrecarga de desempenho tipicamente associada à implementação manual de FHE, visando viabilizar computação preservadora de privacidade para aplicações do mundo real.

## Arquitetura e Uso

Para guias detalhados de implementação, exemplos e a estrutura do código-fonte, por favor consulte o subdiretório [`transpiler`](./transpiler/).

## Suporte e Legado

Embora este repositório continue a receber atualizações críticas, o desenvolvimento ativo e as melhorias de grandes funcionalidades estão focados no projeto **HEIR**. Não estamos aceitando contribuições externas para este repositório legado específico no momento.