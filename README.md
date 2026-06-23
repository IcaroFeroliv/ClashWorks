# ClashWorks 🚀

Um plugin avançado para Autodesk Revit focado em acelerar o processo de resolução de interferências (Clashes) vindas do Navisworks.

O **ClashWorks** lê relatórios HTML exportados do Navisworks e cria um painel interativo (Dockable Pane) diretamente na interface do Revit. Com um clique, os elementos conflitantes são localizados, isolados e exibidos em uma vista 3D.

## ✨ Principais Funcionalidades

* **Integração Fluida:** Lê relatórios HTML do Navisworks, mapeando dinamicamente as colunas, mesmo que tenham sido exportadas em ordens diferentes.
* **Isolamento 3D Automático:** Cria e gerencia uma vista 3D ("FluxoMEP - Análise de Clash"), aplicando uma Section Box com 1 metro de margem ao redor dos elementos conflitantes.
* **Suporte a Grupos e Comentários:** O plugin identifica automaticamente os grupos criados no Navisworks e exibe os comentários do coordenador BIM com uma interface moderna (UI Card).
* **Memória Inteligente (Cache Local):** Salva o progresso da sua sessão em um arquivo `.json` no `AppData`. Clashes marcados como "Resolvidos" permanecem resolvidos mesmo que o Revit seja reiniciado ou o relatório seja recarregado.
* **Prevenção de Erros:** Ignora elementos que estão em vínculos (Links) de forma segura.

## 🛠️ Como Instalar

1. Vá até a aba [Releases]([link-para-a-sua-aba-releases](https://github.com/IcaroFeroliv/ClashWorks/releases/tag/v1.0.0)) deste repositório.
2. Baixe o instalador mais recente (`ClashWorks_Installer.exe`).
3. Execute a instalação.
4. Abra o Revit. O botão estará disponível na aba **Suplementos (Add-Ins)**.

## 📖 Como Usar

1. No **Navisworks**, exporte o seu relatório de interferências no formato **HTML (Tabular)**.
2. No **Revit**, clique no botão **ClashWorks** na aba *Suplementos*.
3. No painel lateral, clique em "Carregar Relatório" e selecione o arquivo HTML.
4. Clique em qualquer clash da lista para focar a câmera automaticamente nos elementos.
5. Após corrigir a modelagem, clique em **Marcar como Resolvido** para limpar a sua lista.

## 💻 Tecnologias Utilizadas
* C# (.NET Framework)
* Revit API
* WPF (Windows Presentation Foundation) para UI/UX
* HtmlAgilityPack (Parsing do relatório HTML)
* Newtonsoft.Json (Sistema de memória de sessão)
