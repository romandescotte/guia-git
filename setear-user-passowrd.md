Cambiaron los metodos de autenticacion, antes era:

git config --global user.email "you@example.com"
  
git config --global user.name "Your Name"

Ahora hay que instalar git CLI:

curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null

sudo apt update

sudo apt install gh

Despues ejecutar: gh auth login

Which account do you want to log into: GitHub.com
What is your preferred protocol por Git operations? HTTPS
Authenticate Git with your GitHub credentiales? Yes
How would you like to authenticate GitHub CLI? Pegar token obtenido den GitHub.com

mas info de autenticacion en: https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/


