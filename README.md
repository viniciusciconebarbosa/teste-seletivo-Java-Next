# 🌳 Analisador de Hierarquia de Palavras (Full-Stack)

> **Status:** Concluído ✔️ | Desafio Técnico Nível Pleno

## 💻 Sobre o Projeto
Este projeto full-stack foi desenvolvido como solução para um desafio técnico focado em processamento de estruturas de dados complexas (Árvores/Nós) e otimização de performance. 

O sistema é composto por duas frentes:
1. **Back-End (Java CLI):** Uma interface de linha de comando otimizada que carrega um arquivo JSON representando uma árvore hierárquica e analisa em qual nível de profundidade determinadas palavras de uma frase se encontram.
2. **Front-End (Next.js & TypeScript):** Uma aplicação web intuitiva que permite ao usuário construir visualmente essa árvore de categorias infinitas e exportar o arquivo JSON formatado corretamente para ser consumido pela CLI.

## 🛠️ Tecnologias Utilizadas

**Back-End:**
* Java (Aplicação de Linha de Comando - CLI)
* Estrutura de Dados (Árvores de Busca N-árias)
* JUnit (Testes de estresse e validação lógica)

**Front-End:**
* Next.js & React
* TypeScript
* Manipulação de estado complexo e exportação de arquivos nativa

## ⚙️ Arquitetura e Diferenciais Técnicos

* **Performance em Tempo de Execução:** A CLI foi construída com foco em eficiência. A flag `--verbose` rastreia o tempo exato (em milissegundos) do carregamento do JSON na memória e da varredura das palavras.
* **Testes de Estresse:** O back-end conta com cobertura de testes unitários, incluindo a análise de inputs massivos (strings com mais de 5000 caracteres) para garantir que não haja estouro de memória ou lentidão na busca.
* **Desacoplamento:** O front-end e o back-end operam de forma independente, comunicando-se unicamente através do contrato de dados via arquivo JSON gerado dinamicamente.

## 🚀 Como Executar o Projeto Localmente

### 1. Rodando o Analisador Back-End (CLI)
Pré-requisito: Ter o Java instalado. O executável lê os dados da pasta `dicts/`.

No terminal, execute o comando seguindo a sintaxe de análise de profundidade (`--depth`):
```bash
java -jar cli.jar analyze --depth 2 "Eu vi gorilas e papagaios" --verbose
