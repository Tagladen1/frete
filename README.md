<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CRUD LocalStorage</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"/>
</head>
<body class="p-4">
  <h1>CRUD com LocalStorage</h1>

  <button class="btn btn-primary mb-3" onclick="crud.showForm()">Novo Registro</button>
  <button class="btn btn-secondary mb-3" onclick="crud.download()">Baixar JSON</button>

  <table class="table table-striped">
    <thead>
      <tr>
        <th>ID</th>
        <th>Campo Principal</th>
        <th>Ações</th>
      </tr>
    </thead>
    <tbody id="crud-list"></tbody>
  </table>

  <!-- Modal -->
  <div class="modal fade" id="crudModal" tabindex="-1">
    <div class="modal-dialog modal-xl">
      <div class="modal-content">
        <form id="crud-form">
          <div class="modal-header">
            <h5 class="modal-title">Formulário...</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body" id="form-container"></div>
          <div class="modal-footer">
            <button type="submit" class="btn btn-success">Salvar</button>
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancelar</button>
          </div>
        </form>
      </div>
    </div>
  </div>
<template id="form-template">
    <div class="row">
    <div class="col-md-4">
      <label for="cod" class="form-label">Código do produto:</label>
      <input type="cod" class="form-control" name="cod" required>
    </div>
    <div class="col-md-8">
      <label for="desc" class="form-label">Descrição do produto:</label>
      <input type="desc" class="form-control" name="desc" required>
    </div>
    <div class="col-md-3">
      <label for="quant" class="form-label">Quantidade em estoque:</label>
      <input type="quant" class="form-control" name="quant" required>
    </div>
    <div class="col-md-3">
      <label for="larg" class="form-label">Largura do pacote(cm):</label>
      <input type="larg" class="form-control" name="larg" required>
    </div>
     <div class="col-md-3">
      <label for="art" class="form-label">Altura do pacote(cm):</label>
      <input type="art" class="form-control" name="alt" required>
    </div>
     <div class="col-md-3">
      <label for="larg" class="form-label">Profundidade do pacote(cm):</label>
      <input type="larg" class="form-control" name="larg" required>
    </div>
     <div class="col-md-6">
      <label for="larg" class="form-label">Peso do pacote(kg):</label>
      <input type="larg" class="form-control" name="larg" required>
    </div>
     <div class="col-md-6">
      <label for="larg" class="form-label">Preço de venda(R$):</label>
      <input type="larg" class="form-control" name="larg" required>
    </div>
    </div>
</template>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script src="crud.js"></script>
</body>
</html>
