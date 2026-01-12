# 📋 Tabela de Indicações para Promoções/Transferências

Sistema web desenvolvido para facilitar, padronizar e validar o processo de indicações de promoções, transferências e méritos para o Comitê de Pessoas/RH. A ferramenta permite o preenchimento de dados, validação de regras de negócio em tempo real e exportação de documentos oficiais.

---

## 🚀 Funcionalidades Principais

* **Gerenciamento Dinâmico:** Adição e remoção de linhas conforme a necessidade do gestor.
* **Validação de Dados:**
    * Verificação de campos obrigatórios.
    * Validação de formatos (Matrícula numérica, Cód. Setor).
    * Detecção de matrículas duplicadas.
* **Regras de Negócio Automatizadas:** Bloqueios automáticos para garantir a conformidade com as normas de RH (detalhes abaixo).
* **Exportação de Documentos:**
    * **PDF:** Geração de arquivo pronto para impressão/envio (Layout A4 Paisagem).
    * **Excel/CSV:** Exportação de dados estruturados para processamento pela equipe de Remuneração.
* **Interface Amigável:**
    * Navegação via teclado (Setas, Tab, Enter).
    * Ordenação avançada (Multi-nível) e rápida (clique no cabeçalho).
    * Campos de data híbridos (Seleção de Data ou "N/A").

---

## 🔒 Regras de Negócio e Bloqueios

O sistema possui travas de segurança para impedir o envio de informações inconsistentes:

1. **Cargo de Liderança:**
    * Se `Cargo Proposto é de Liderança?` = **SIM** e `R&S fez Avaliação?` = **NÃO**:
    * 🛑 **Ação:** O sistema **bloqueia** a geração de PDF/Excel até que a pendência seja resolvida.

2. **Empregado em Treinamento:**
    * Se `Em Treinamento?` = **SIM** e `Possui Carta?` = **NÃO**:
    * 🛑 **Ação:** O sistema **bloqueia** a geração dos arquivos e lista nominalmente os colaboradores pendentes.

3. **Matrículas Duplicadas:**
    * O sistema impede a exportação caso a mesma matrícula seja inserida mais de uma vez na lista.

4. **Substituição:**
    * Campos relacionados ao empregado substituído são habilitados/desabilitados dinamicamente com base na seleção de "É Substituição?".

---

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido utilizando tecnologias web padrão (Vanilla), sem necessidade de instalação de dependências complexas (Node.js, Python, etc.) para rodar.

* **HTML5:** Estrutura semântica.
* **CSS3:** Estilização responsiva, variáveis (CSS Variables) e layout flexbox/grid.
* **JavaScript (ES6+):** Lógica de validação, manipulação do DOM e regras de negócio.
* **Bibliotecas Externas (via CDN):**
    * `jspdf`: Motor de geração de PDF.
    * `html2pdf.js`: Conversão do DOM HTML para Canvas/PDF.

---

## ⌨️ Atalhos de Teclado

Para agilizar o preenchimento por usuários avançados:

| Atalho | Ação |
| :--- | :--- |
| `Ctrl + M` | Criar Nova linha |
| `Ctrl + P` | Abrir modal de geração de PDF |
| `Ctrl + E` | Exportar para Excel/CSV |
| `F1` | Abrir Instrucoes de Uso |
| `Setas` | Navegar entre as células |

---

## 📦 Como Utilizar

1. Baixe o arquivo `FormularioIndicações.html` (ou o nome final do arquivo).
2. Abra o arquivo em qualquer navegador web moderno (Chrome, Edge, Firefox).
3. Preencha o cabeçalho (Responsável e Empresa).
4. Insira os dados dos colaboradores.
5. Utilize os botões no rodapé ou atalhos para gerar os relatórios.

---

## 👨‍💻 Autor

Desenvolvido por **Alan Silva**.
