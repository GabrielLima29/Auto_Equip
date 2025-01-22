# Auto.Equip

# *Instruções para Rodar o Projeto*

Este guia fornece um passo a passo para clonar e configurar o projeto Laravel "WorkDone" utilizando Git Flow.

## *1. Clonar o Projeto do GitHub*

1. **Abrir o Prompt de Comando**: 
   - Abra o terminal no Visual Studio Code ou no CMD.

2. **Executar o Comando**:
   ```bash
   git clone https://github.com/GabrielLima29/Auto_Equip.git

### *1.1 Mudando de Branch*
- Por padrão, o Git irá clonar a branch main. Para trabalhar na branch develop, execute:
    ```bash
    git checkout develop
- Verificação: Verifique se os arquivos estão diferentes, especialmente se todas as migrations estão na pasta database/migrations. Na branch main, devem aparecer apenas 4 arquivos, enquanto na branch develop, você verá várias migrations.

## *2. Criar o .env e a pasta vendor*
1. Navegar para a Pasta do Projeto:
   ```
   cd Auto_Equip
2. Dar ínicio ao GitFlow:
   ```
   git flow init
## *3. Versionamento*
Ao trabalhar em equipe, é importante evitar conflitos. Siga estas orientações para versionamento:

### *3.1. Atualizar o Repositório*
- Antes de iniciar qualquer nova tarefa, sempre execute o comando abaixo para garantir que você tenha a versão mais recente do repositório:
  ```bash
  git pull

### *3.2. Criar uma Nova Feature*
- Para iniciar uma nova feature, utilize o comando:
  ```bash
  git flow start feature <nome_da_feature>
- Exemplo:
  ```bash
  git flow start feature fix_bug_login
- Fazer Alterações: Realize as alterações necessárias para cumprir o objetivo da feature.

### *3.3. Adicionar e Comitar Alterações*
1. Adicione todos os arquivos alterados:
    ```bash
    git add . 
2. Realize um commit com uma descrição clara das alterações:
    ```bash
    git commit -m "Descrição das alterações"

### *3.4. Versionamento de Releases*
- Para seguir o controle de versões, crie uma versão utilizando o padrão (patch, minor e major):
    ```bash
    git tag -a v1.0.0 -m "Descrição da versão"
- *Importante*: Modifique a versão conforme necessário antes de rodar o comando acima.

### *3.5. Finalizar a Feature*
- Para encerrar a feature e voltar à branch develop, execute:
    ```bash
    git flow finish feature <nome_da_feature>
