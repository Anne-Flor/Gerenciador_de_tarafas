## Instruções de uso deste repositório

Vamos seguir a recomendação do professor, cada desenvolvedor vai trabalhar em uma branch separadamente. As branches, ou ramos, no Git são uma maneira de criar versões paralelas de um projeto. Elas permitem que você trabalhe em diferentes funcionalidades ou correções de bugs sem afetar o código principal do projeto.
 
 Por exemplo, para criar uma branch chamada `feature-new-feature`, você usaria o seguinte comando:
 ```bash
git branch feature-new-feature
```
Depois de criar uma branch, você pode começar a fazer alterações no código. Todas as alterações que você fizer serão rastreadas na branch. 

Após as modificações sugeridas na branch forem validadas a branch em questão será mergeada na branch principal(`main`).
A branch `main` será a versão final do projeto (após todos os PRs forem revisados e mergeadas)

## Como deploiar este projeto localmente

### Softwares necessários
Certifique-se que tenha os seguintes softwares instalados:
- PHP 8.x
- nodejs v16.x
- npm
- composer
- MySQL (ou MariaDB)

Após clonar este repositório e entrar no diretorio, efetue os seguintes commandos:

```bash
# Dependencias do PHP 
composer update
# Modulos node
npm install
# Compilar assets (CSS e JS)
npm run build
# Criar base de dados e estrutura de tabelas
php artisan migrate
```
Se tudo der certo será possivel executar o servidor web de desenvolvimento do Laravel
```bash
php artisan server
```
Enquanto este comando tiver em execução será possivel acessar o front-end no endereço local http://127.0.0.1:8000

Caso deseje execute em um outro terminal o servidor dinâmico de assets(VITE) para que os assets sejam recompilados assim que seus arquivos de template forem atualizados.

```bash
npm run dev
```

:warning: Caso seja necessario edite o arquivo `.env` para utilizar configurações especificas do seu ambiente, como usuário e senha do MySQL.