# **Conversor JSON/CSV para DBF**  

## 📌 **Descrição do Projeto**  
Este projeto é um pacote desenvolvido para converter arquivos **JSON** e **CSV** para o formato **DBF**. Ele foi projetado para oferecer uma solução moderna e eficiente para manipulação de arquivos **dBase**, amplamente utilizados em sistemas governamentais e aplicações legadas.  

O conversor utiliza **Bun** e segue princípios de **Domain-Driven Design (DDD)** para garantir modularidade, escalabilidade e facilidade de manutenção.  

## 📌 **Motivação**  
Muitos sistemas antigos ainda utilizam arquivos **.DBF** devido à compatibilidade com softwares legados e sua adoção em órgãos governamentais, como SINAN, SIA/SUS e SEFIP. No entanto, ferramentas modernas para conversão e manipulação desses arquivos são escassas e limitadas.  

Este projeto resolve esse problema ao fornecer um **conversor rápido, eficiente e atualizado**, permitindo uma transição fluida entre **DBF**, **JSON** e **CSV**.  

## 🚀 **Principais Recursos**  
✅ **Conversão Automática** de JSON/CSV para DBF  
✅ **Suporte a Diferentes Tipos de Dados** (`Character`, `Numeric`, `Date`, `Logical`, `Float`,`Float`)  
✅ **Validação Estrutural** antes da conversão  
✅ **Arquitetura Modular** baseada em **DDD (Domain-Driven Design)**  
✅ **Otimizado com Bun** para alto desempenho  
✅ **Facilidade de Integração** com sistemas modernos  

## 📂 **Arquitetura**  
O sistema é dividido em diferentes **Bounded Contexts**, garantindo separação de responsabilidades:  

- **DBFFileDefinition** → Gerencia a estrutura dos arquivos `.DBF`.  
- **DBFFieldManagement** → Gerencia os campos dentro do `.DBF`.  
- **DBFRecordManagement** → Manipula os registros dentro do `.DBF`.  
- **DBFValidation** → Valida a estrutura e os dados dos arquivos `.DBF`.  
- **DBFExport** → Exporta a estrutura interna para um arquivo `.DBF` válido.  
- **DBFImport** → Converte arquivos JSON/CSV para `.DBF`.  

## 🔧 **Instalação**  
Para instalar o pacote e utilizá-lo em seu projeto, execute:  

```sh
bun install conversor-dbf
```

## 📌 **Tipos de Dados Suportados**  
| Tipo | Descrição | Tamanho Máximo |
|------|------------|----------------|
| `C` (Character) | Texto | 10 bytes |
| `N` (Numeric) | Números inteiros/decimais | 19 bytes |
| `F` (Float) | Números de ponto flutuante | 19 bytes |
| `L` (Logical) | Booleano (`T` ou `F`) | 1 byte |
| `D` (Date) | Datas (`YYYYMMDD`) | 8 bytes |

## 🏗 **Futuro Desenvolvimento**  
🔹 Suporte a exportação para **XML, YAML e Parquet**  
🔹 Integração com bancos relacionais (**PostgreSQL, MySQL, SQLite**)  
🔹 Otimizações para **manipulação de grandes volumes de dados**  

## 📜 **Licença**  
Este projeto é desenvolvido e mantido pela **Envolve** e está sob a licença **GNU Affero General Public License v3.0 (AGPL-3.0)**.  
