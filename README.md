# Desafio-do-Amigo-Secreto
Desafio de conclusão da formação Iniciante em programação da Alura.
# Funcionalidades
Sorteio de amigo secreto
Função para garantir que uma pessoa não aposente seu próprio nome como amigo secreto
Função otimizada de embaralhamento da lista de pessoas
# Tecnologia Aplicada
Javascript, HTML, CSS
# Uso/Exemplos
# Adicionar Amigo
function adicionarAmigo(){
    const input = document.getElementById("amigo")
    let nome = input.value;

if(nome === "" || !isNaN(nome)) {
    alert("Por favor, insira um nome válido.");
    return;
  }

  amigos.push(nome);
  atualizarLista();

  input.value = "";
}

# Função atualizar lista
 const lista = document.getElementById("listaAmigos");
    (lista.innerHTML = ""),
      amigos.forEach((amigo, index) => {
        const li = document.createElement("li");
        li.textContent = amigo + (index < amigos.lenght - 1 ? "," : "");
        lista.appendChild(li);
      });
  }

  # Função sortear amigo
function sortearAmigo() {
    if (amigos.lenght === 0) {
      alert("A lista de amigos está vazia.");
      return;
    }
  
    if (amigos.length <= 2) {
      alert("Para poder realizar o sorteio, é preciso ter três amigos ou mais.");
      return;
    }
  
    let indiceSorteado = Math.floor(Math.random() * amigos.length);
  
    let amigoSorteado = amigos[indiceSorteado];
  
    sorteados.push(amigoSorteado);
  
    const resultado = document.getElementById("resultado");
    resultado.innerHTML = "O amigo secreto sorteado é: " + sorteados;
  
    dispararConfete();
  
    sorteados = [];
  
    atualizarLista();
  }
  # Autor
  @NathaliaSorregotti
