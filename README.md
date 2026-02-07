# api-rest-php
index.php
<?php
header("Content-Type: application/json");

$method = $_SERVER['REQUEST_METHOD'];

$clientes = [
  ["id" => 1, "nome" => "Maria"],
  ["id" => 2, "nome" => "João"]
];

if ($method === "GET") {
  echo json_encode($clientes);
}

if ($method === "POST") {
  echo json_encode([
    "mensagem" => "Cliente criado com sucesso"
  ]);
}

if ($method === "DELETE") {
  echo json_encode([
    "mensagem" => "Cliente removido"
  ]);
}
