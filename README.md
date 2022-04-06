# recrutamento-front-end

Criar uma pagina de Area do cliente Alterdata

- Deve seguir o layout disponivel em https://xd.adobe.com/view/d1d5f4f6-0e92-41ce-81a9-98e4751cede2-8486/specs/
	- O login sempre vai ser no formato codigo.nome, exemplo: 123456.teste
	- A senha não pode conter o codigo ou login do usuário
	- A senha não pode conter espacos
	- Pode ser desconsiderado o botao "Este ano" do layout
	- Desabilitar o botão de cadastrar usuário caso o cliiente já tenha atingido o limite de usuários criados

- Caso você deseje utilizar um back-end ja pronto o mesmo deve ser solicitado e deve seguir os seguinte passos para consumir o mesmo :
	- Criar uma conta no mongoDB ou instalar o mongoDB na sua maquina
	- Preencher as variaveis do mongoDB no arquivo .env
	- Executar yarn ou npm install na raiz para instalar as dependecias
	- Executar yarn dev ou npm run dev para inciar o back end
	
Rotas do back-end caso utilize o exemplo pronto :
	
  - Create user

		Url : localhost:3333/user
		Body: {
			"codigo":"123456",
			"login":"123456.marcus",
			"password":"123456.marcus",
			"email":"marcustere28@gmail.com"
		}
		Metodo: POST
	
	
- Reset password
	
		Url : localhost:3333/resetpassword
		Body:{
			"login":"123456.marcus",
			"password":"123456.marcus"
		}
		Metodo: PUT
	
- Update user email 
	
		Url : localhost:3333/user
		Body: {
			"login":"123456.marcus",
			"email":"marcus.dsn.nuvem@alterdata.com.br"
		}
		Metodo: PUT
		
- List All Users
	 
		Url : localhost:3333/users
		Metodo: GET
		
- Delete user
	
		Url : localhost:3333/user
		Body: {
			"login":"123456.marcus"
		}
		Metodo: DELETE


Caso deseje criar o seu proprio back-end  basta seguir as informacoes disponiveis em https://github.com/alterdata-nuvem/recrutamento-back-end

