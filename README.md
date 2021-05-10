<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CRUD </title>

    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css"
        integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
 <link rel="stylesheet" href="font-awesome-4.7.0/font-awesome-4.7.0/css/font-awesome.min.css">
</head>

<body>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-12">
                <h3>Formulário de Cadastro de clientes</h3>
            </div>
        </div>
    </div>
    <div class="col-md-12">
        <button type="button" class="btn btn-primary float-right" data-toggle="modal"
            data-target="#modalRegistro">Adicionar </button>
    </div>
    <div class="row" style="margin-top: 45px">
        <div class="col-md-12">
            <table id="tblDados" class="table table-hover table-dark">
                <thead>
                    <tr>
                        <th scope="col">#</th>
                        <th scope="col">Nome</th>
                        <th scope="col">E-mail</th>
                        <th scope="col">CPF ou CNPJ</th>
                        <th scope="col">Telefone</th>
                        <th scope="col">CEP</th>
                        <th scope="col">Logradouro</th>
                        <th scope="col">Número</th>
                        <th scope="col">Bairro</th>
                        <th scope="col">Cidade</th>
                        <th scope="col">Estado</th>
                        <th scope="col" style="width: 50px;"></th>
                        <th scope="col" style="width: 50px;"></th>
                    </tr>
                </thead>
                <tbody>

                </tbody>
            </table>

        </div>
    </div>

    <!-- Modal -->
    <div class="modal fade" id="modalRegistro" tabindex="-1" role="dialog" aria-labelledby="modalRegistroLabel"
        aria-hidden="true">
        <div class="modal-dialog modal-lg" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="modalRegistroLabel">Registros</h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Fechar">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>

                <div class="modal-body">
                    <div class="row">
                        <div class="col-md-6">
                            <div class="form-group">
                                <label for="">Nome</label>
                                <input id="txtNome" type="text" class="form-control" placeholder="digitel o nome..." />
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="form-group">
                                <label for="">Email</label>
                                <input id="txtEmail" type="text" class="form-control" placeholder="digitel o Email...">
                            </div>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-md-6">
                            <div class="form-group">
                                <label for="">CPF ou CNPJ</label>
                                <input id="txtCpfCnpj" type="txt" class="form-control"
                                    placeholder="Digite o CPF ou CNPJ..." />
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="form-group">
                                <label type="text">Telefone</label>
                                <input id="txtTelefone" type="txt" class="form-control"
                                    placeholder="Digite o Telefone..." />
                            </div>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-md-6">
                            <div class="form-group">
                                <label for="">CEP</label>
                                <input id="txtCep" type="txt" class="form-control" placeholder="Digite o CEP..." />
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="form-group">
                                <label type="text">Logradouro</label>
                                <input id="txtLogradouro" type="txt" class="form-control"
                                    placeholder="Digite o Logradouro..." />
                            </div>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-md-6">
                            <div class="form-group">
                                <label for="">Número</label>
                                <input id="txtNumero" type="txt" class="form-control"
                                    placeholder="Digite o Numero..." />
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="form-group">
                                <label type="text">Bairro</label>
                                <input id="txtBairro" type="txt" class="form-control"
                                    placeholder="Digite o Bairro..." />
                            </div>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-md-6">
                            <div class="form-group">
                                <label for="">Cidade</label>
                                <input id="txtCidade" type="txt" class="form-control"
                                    placeholder="Digite a Cidade..." />
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="form-group">
                                <label type="text">Estado</label>
                                <input id="txtEstado" type="txt" class="form-control"
                                    placeholder="Digite o Estado..." />
                            </div>
                        </div>
                    </div>

                </div>

                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-dismiss="modal">Fechar</button>
                    <button id="btnSalvar" type="button" class="btn btn-primary">Salvar mudanças</button>
                </div>
            </div>
        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
        integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
        crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"
        integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49"
        crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"
        integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy"
        crossorigin="anonymous"></script>

    <script src="index.js"></script>
</body>

</html>
