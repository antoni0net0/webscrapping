# 🛒 Projeto de Automação Web — Busca de Preços

## 📌 Objetivo

Este projeto tem como propósito **treinar habilidades de automação web utilizando o Selenium** para capturar e monitorar informações de preços de produtos em sites de e-commerce.

Imagine que você trabalha na área de **compras de uma empresa** e precisa constantemente comparar preços entre fornecedores para encontrar os melhores negócios. Com essa automação, você não precisa mais fazer isso manualmente!

---

## ⚙️ Como Funciona

1. **Leitura de uma planilha de produtos**, contendo:
   - Nome do produto
   - Preço máximo de compra
   - Preço mínimo aceitável (evita produtos errados ou suspeitos)
   - Palavras-chave que devem ser evitadas na busca

2. **Busca automatizada** dos produtos no Google Shopping (e opcionalmente em outros sites como o Buscapé), extraindo os preços e links dos produtos.

3. **Filtragem inteligente** dos resultados:
   - Somente produtos com preço entre o mínimo e o máximo são considerados válidos.
   - Produtos com palavras indesejadas no título são descartados.

4. **Geração de uma tabela** com os produtos válidos encontrados, contendo:
   - Nome do produto
   - Preço
   - Loja
   - Link de compra

5. **Envio automático de um e-mail** contendo a tabela com os produtos encontrados abaixo do limite de preço, diretamente para o endereço de e-mail definido.

---

## 📄 Exemplo da Planilha de Entrada

| Produto        | Preço Máximo | Preço Mínimo | Termos Banidos        |
|----------------|--------------|--------------|------------------------|
| iPhone 12 64GB | 3500         | 2000         | usado, recondicionado  |
| RTX 3060       | 2800         | 1500         | mineradora, defeito    |

---

## 📧 Exemplo do E-mail Gerado

> **Assunto:** Produto(s) Encontrado(s) na faixa de preço desejada  
>
> Prezados,  
>
> Encontramos alguns produtos em oferta dentro da faixa de preço desejada. Segue tabela com detalhes:  
>
> *(tabela com nome, preço, loja e link do produto)*  
>
> Qualquer dúvida, estou à disposição.  
>
> Att.

---

## 🧰 Tecnologias Utilizadas

- Python 🐍
- Selenium 🌐
- Pandas 📊
- Outlook (via `pywin32`) para envio de e-mails 📧

---

## 🧪 Possíveis Melhorias Futuras

- 🔍 Adicionar suporte a mais sites (ex: Zoom, Amazon, Magazine Luiza)
- 📥 Baixar automaticamente imagens dos produtos
- 📊 Exportar a tabela de resultados em PDF ou Excel com formatação
- ⏰ Agendar a automação para rodar periodicamente (com `cron` ou `Task Scheduler`)
- 🖥 Criar uma interface gráfica simples (com Tkinter, PyQt ou Web)
- 📈 Gerar relatórios históricos para acompanhar a variação de preços ao longo do tempo
- 🌐 Implementar um sistema web com dashboard para visualização dos dados em tempo real
