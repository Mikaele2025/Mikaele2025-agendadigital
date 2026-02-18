function entrar() {
  const tipo = document.getElementById("tipoUsuario").value;

  if (tipo === "professor") {
    window.location.href = "professor.html";
  } else {
    window.location.href = "pais.html";
  }
}

// Salvar dados no navegador (localStorage)
const form = document.getElementById("formRotina");

if (form) {
  form.addEventListener("submit", function(e) {
    e.preventDefault();

    const registro = {
      nome: document.getElementById("nomeAluno").value,
      alimentacao: document.getElementById("alimentacao").value,
      sono: document.getElementById("sono").value,
      atividades: document.getElementById("atividades").value,
      observacoes: document.getElementById("observacoes").value,
      data: new Date().toLocaleDateString()
    };

    let registros = JSON.parse(localStorage.getItem("agenda")) || [];
    registros.push(registro);
    localStorage.setItem("agenda", JSON.stringify(registros));

    alert("Registro salvo com sucesso!");
    form.reset();
  });
}

// Mostrar dados para os pais
const lista = document.getElementById("listaRegistros");

if (lista) {
  let registros = JSON.parse(localStorage.getItem("agenda")) || [];

  registros.forEach(r => {
    lista.innerHTML += `
      <div class="card">
        <h3>${r.nome}</h3>
        <p><strong>Data:</strong> ${r.data}</p>
        <p><strong>Alimentação:</strong> ${r.alimentacao}</p>
        <p><strong>Sono:</strong> ${r.sono}</p>
        <p><strong>Atividades:</strong> ${r.atividades}</p>
        <p><strong>Observações:</strong> ${r.observacoes}</p>
        <hr>
      </div>
    `;
  });
}
