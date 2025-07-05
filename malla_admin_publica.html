<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Malla Interactiva - Administración Pública</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f9f9f9;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
    }
    .semestre {
      margin-bottom: 30px;
    }
    .semestre h2 {
      margin: 10px 0;
    }
    .ramos {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }
    .ramo {
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      cursor: pointer;
      min-width: 180px;
      text-align: center;
      transition: background 0.3s;
    }
    .bloqueado {
      background: #ddd;
      color: #666;
    }
    .disponible {
      background: #fff3cd;
      color: #000;
    }
    .aprobado {
      background: #c3e6cb;
      color: #000;
    }
  </style>
</head>
<body>
  <h1>Malla Interactiva - Administración Pública</h1>
  <div id="contenedor"></div>

  <script>
    const ramos = {
      // Ejemplo de estructura mínima (los reales los agregaré a partir de tu malla completa)
      "Inducción a la Formación Profesional": {
        semestre: 1,
        requisitos: []
      },
      "Teoría de la Administración": {
        semestre: 1,
        requisitos: []
      },
      "Administración Pública": {
        semestre: 3,
        requisitos: ["Teoría de la Administración"]
      },
      "Adm. Pública Chilena": {
        semestre: 4,
        requisitos: ["Administración Pública"]
      }
    };

    const estado = JSON.parse(localStorage.getItem("estadoMalla")) || {};

    function guardarEstado() {
      localStorage.setItem("estadoMalla", JSON.stringify(estado));
    }

    function estaDisponible(nombre) {
      const reqs = ramos[nombre].requisitos;
      return reqs.every(r => estado[r] === "aprobado");
    }

    function render() {
      const contenedor = document.getElementById("contenedor");
      contenedor.innerHTML = "";
      const porSemestre = {};

      for (const [nombre, info] of Object.entries(ramos)) {
        if (!porSemestre[info.semestre]) porSemestre[info.semestre] = [];
        porSemestre[info.semestre].push(nombre);
      }

      Object.keys(porSemestre).sort((a, b) => a - b).forEach(sem => {
        const divSem = document.createElement("div");
        divSem.className = "semestre";
        divSem.innerHTML = `<h2>Semestre ${sem}</h2>`;

        const divRamos = document.createElement("div");
        divRamos.className = "ramos";

        porSemestre[sem].forEach(nombre => {
          const div = document.createElement("div");
          div.className = "ramo";
          const estadoRamo = estado[nombre];
          if (estadoRamo === "aprobado") {
            div.classList.add("aprobado");
          } else if (estaDisponible(nombre)) {
            div.classList.add("disponible");
          } else {
            div.classList.add("bloqueado");
          }

          div.innerText = nombre;
          div.onclick = () => {
            if (!estaDisponible(nombre) && estado[nombre] !== "aprobado") return;
            estado[nombre] = estado[nombre] === "aprobado" ? undefined : "aprobado";
            guardarEstado();
            render();
          };

          divRamos.appendChild(div);
        });

        divSem.appendChild(divRamos);
        contenedor.appendChild(divSem);
      });
    }

    render();
  </script>
</body>
</html>
