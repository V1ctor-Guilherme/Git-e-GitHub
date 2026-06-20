<div align="center"><img src="./img/capa.png"></div>

# Fundamentos Git e GitHub

Este repositório é um espaço dedicado a centralizar anotações de estudo e resumos práticos sobre controle de versão. O objetivo principal é documentar a jornada de aprendizado, desmistificando os conceitos e criando uma base sólida de conhecimento para consultas rápidas.

## Objetivos de Aprendizagem

* **Compreender o conceito de versionamento:** Entender como ele elimina a necessidade de criar várias cópias do mesmo arquivo (o famoso trabalho-final-v2.doc) e protege o histórico do projeto.
* **Diferenciar o Git do GitHub:** Ter clareza absoluta de que o Git é o "motor" que roda no seu computador, enquanto o GitHub é a "nuvem" onde você armazena e compartilha seu código.
* **Dominar a arquitetura local do Git:** Entender a jornada de um arquivo através das três áreas principais: Diretório de Trabalho (Working Directory), Área de Preparação (Staging Area) e Histórico/Repositório (Repository).
* **Entender a dinâmica da nuvem:** Compreender o que são repositórios remotos e a diferença entre enviar código (Push) e baixar código (Pull).
* **Executar o ciclo básico na prática:** Conseguir abrir o terminal, iniciar um repositório do zero, registrar alterações (git init, git add, git commit) e enviar o seu projeto de forma segura para o GitHub (git push).

## Versionamento de Código

O versionamento (ou controle de versão) é um sistema responsável por registrar e gerenciar todas as alterações feitas em um arquivo ou conjunto de arquivos ao longo do tempo.

**O problema que ele resolve:** <br />A principal utilidade do controle de versão é eliminar a prática de salvar múltiplas cópias de um mesmo trabalho para não perder o progresso (ex: `projeto.txt`, `projeto_v2.txt`, `projeto_final_agora_vai.txt`). Ele organiza e automatiza esse processo.

Em vez de duplicar arquivos, o sistema atua como uma "máquina do tempo". Ele salva "fotografias" (estados) do seu projeto em momentos específicos, permitindo a navegação por toda a linha do tempo do desenvolvimento.

**Principais vantagens:**

* **Histórico Detalhado:** Permite saber exatamente **quem** alterou o código, **o que** foi modificado, **quando** ocorreu a mudança e o **porquê** (através das mensagens de registro).
* **Segurança e Reversão (Rollback):** Se uma nova linha de código quebrar o sistema, é possível reverter o projeto de forma cirúrgica para a última versão funcional.
* **Trabalho em Paralelo:** É a base para o trabalho em equipe na área de tecnologia. Permite que várias pessoas alterem o mesmo projeto simultaneamente, unindo o trabalho de todos de forma inteligente no final, sem sobreposições destrutivas.
* **Experimentação Segura:** Possibilita criar ramificações (linhas do tempo paralelas) para testar novas ideias sem risco de comprometer o projeto principal.

## Git

O **Git** é o sistema de controle de versão mais utilizado no mundo, criado em 2005 por Linus Torvalds (o mesmo criador do sistema operacional Linux). Ele é classificado como um sistema de controle de versão **distribuído**. Isso significa que cada computador possui uma cópia local completa de todo o histórico do projeto, não dependendo exclusivamente de um servidor central para a maioria das tarefas.

**Principais características:**
* **Desempenho Local:** Como o histórico completo fica na sua própria máquina, operações como visualizar versões anteriores ou verificar diferenças são quase instantâneas, e não exigem conexão com a internet.
* **Integridade dos Dados:** O Git garante a segurança do código utilizando criptografia (hash SHA-1). É impossível que o histórico seja corrompido ou alterado acidentalmente sem que o sistema detecte.
* **Gestão de Ramificações (Branches):** O Git tornou a criação de ramificações um processo extremamente leve e rápido. Isso facilita a criação de ambientes isolados para desenvolver novas funcionalidades sem afetar a versão principal e estável do projeto.

---

### 1. Como funciona a Arquitetura do Git?

Para dominar o Git, é essencial entender que ele não salva os arquivos de uma vez só. Ele gerencia as alterações transitando os arquivos entre três estados (ou áreas) principais:

| Área | Descrição | Ação / Comando |
| :--- | :--- | :--- |
| **1. Working Directory** (Diretório de Trabalho) | É a pasta do projeto no seu computador. O ambiente real onde você cria, edita ou exclui seus arquivos no dia a dia. | *Edição manual de arquivos* |
| **2. Staging Area** (Área de Preparação) | É a "sala de espera". É o local onde você seleciona e agrupa as alterações específicas que farão parte da próxima versão gravada. | `git add` |
| **3. Repository** (Repositório / Histórico) | É o banco de dados do Git (a pasta oculta `.git`). Onde ele guarda permanentemente o registro (commit) com o estado exato dos seus arquivos. | `git commit` |

**O Ciclo de Vida (Fluxo Básico):**
1. Arquivos são modificados no **Working Directory**.
2. As mudanças desejadas são adicionadas à **Staging Area** (preparadas).
3. O pacote de mudanças na Staging Area é confirmado e gravado de forma permanente no **Repository**.

