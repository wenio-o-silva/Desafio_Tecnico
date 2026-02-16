Desafio Técnico Axion - Backend (API)
Este repositório contém a API desenvolvida para o teste técnico da Axion. A aplicação foi construída utilizando Strapi (Headless CMS) para gerenciar coleções de dados e autenticação de usuários.

Objetivo
O backend serve como a fonte de dados para o frontend, gerenciando as coleções de Pessoas, Comidas e Locais, além de fornecer o sistema de login para candidatos.

Tecnologias e Requisitos
Framework: Strapi v3 (Node.js)

Banco de Dados: SQLite (Local)

Versão do Node.js: >= 14.21.3 (Recomendado o uso de nvm ou fnm)

Como Executar o Servidor
Siga os passos abaixo para rodar a API localmente em sua máquina:

Certifique-se de estar na pasta raiz do backend:
cd backend

Utilize a versão correta do Node.js:
fnm use 14

Instale as dependências do projeto:
npm install

Gere o build administrativo do Strapi:
npm run build

Inicie a aplicação em modo de desenvolvimento:
npm run develop

Após o comando, o servidor estará rodando em http://localhost:1337. Você pode acessar o painel administrativo em http://localhost:1337/admin.

Estrutura de Dados (Collections)
A API foi configurada com três Content Types principais que retornam os dados necessários para a aplicação:

People (Pessoas)

Foods (Comidas)

Places (Locais)

Cada item dentro dessas coleções segue o formato de resposta JSON:

JSON
{
  "name": "Exemplo de Nome",
  "link": "http://localhost:1337/uploads/imagem.jpg"
}
Os campos name são utilizados para as legendas e os campos link fornecem a URL da imagem de fundo para os cards no frontend.

Autenticação
O sistema já conta com um usuário pré-cadastrado no banco de dados SQLite para testes de integração de login:

Identificador: axioner@axion.company

Senha: Axioner123

Observações Técnicas
O banco de dados SQLite está incluso no repositório para garantir que os dados de teste estejam disponíveis imediatamente após o primeiro build.

As permissões de API (Roles & Permissions) foram configuradas para permitir o acesso autenticado aos endpoints das coleções mencionadas.