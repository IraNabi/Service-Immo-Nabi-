function ouvrir(page) {

  document.querySelectorAll(".page").forEach(function(section) {
    section.classList.remove("active");
  });

  document.getElementById(page).classList.add("active");

  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });

  document.getElementById("menu").classList.remove("open");
}


function menu() {

  document.getElementById("menu").classList.toggle("open");

}


function envoyerAnnonce(event) {

  event.preventDefault();

  const nom =
    document.getElementById("nom").value;

  const titre =
    document.getElementById("titre").value;

  const type =
    document.getElementById("type").value;

  const prix =
    document.getElementById("prix").value;

  const lieu =
    document.getElementById("lieu").value;

  const description =
    document.getElementById("description").value;


  const message =
`Bonjour Service Immo Nabi,

Je souhaite publier un bien.

👤 Propriétaire : ${nom}

🏠 Bien : ${titre}

📌 Type : ${type}

💰 Prix : ${prix}

📍 Localisation : ${lieu}

📝 Description :
${description}`;


  const url =
    "https://wa.me/22656304065?text=" +
    encodeURIComponent(message);


  window.open(url, "_blank");

}
