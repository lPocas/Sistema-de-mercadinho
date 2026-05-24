# Sistema-de-mercadinho
Trabalho acadêmico

<!DOCTYPE html>
<html lang="pt-BR">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Mercadinho Seu Zé</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial;
}

body{
    background:#f3f4f6;
}

/* LOGIN */

.login-screen{
    width:100%;
    height:100vh;
    background:linear-gradient(135deg,#14532d,#16a34a);
    display:flex;
    justify-content:center;
    align-items:center;
}

.login-box{
    width:400px;
    background:white;
    padding:40px;
    border-radius:20px;
    box-shadow:0 10px 30px rgba(0,0,0,0.2);
}

.logo{
    text-align:center;
    margin-bottom:30px;
}

.logo i{
    font-size:55px;
    color:#16a34a;
    margin-bottom:10px;
}

.logo h1{
    color:#14532d;
}

.logo p{
    color:gray;
    margin-top:5px;
}

.input-group{
    position:relative;
    margin-bottom:20px;
}

.input-group i{
    position:absolute;
    left:15px;
    top:16px;
    color:#777;
}

.input-group input{
    width:100%;
    padding:15px 15px 15px 45px;
    border:1px solid #ddd;
    border-radius:10px;
    outline:none;
}

.login-btn{
    width:100%;
    padding:15px;
    background:#16a34a;
    border:none;
    color:white;
    border-radius:10px;
    font-size:16px;
    cursor:pointer;
    transition:0.3s;
}

.login-btn:hover{
    background:#15803d;
}

/* SISTEMA */

.system{
    display:none;
}

.sidebar{
    width:250px;
    height:100vh;
    background:linear-gradient(180deg,#0f172a,#14532d);
    position:fixed;
    padding:30px;
}

.sidebar .logo{
    color:white;
}

.sidebar .logo i{
    color:white;
}

.menu{
    margin-top:40px;
}

.menu a{
    display:block;
    color:white;
    text-decoration:none;
    padding:14px;
    margin-bottom:10px;
    border-radius:10px;
    transition:0.3s;
}

.menu a:hover{
    background:#16a34a;
}

.menu a i{
    margin-right:10px;
}

.main{
    margin-left:250px;
    padding:30px;
}

.topbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:30px;
}

.topbar h1{
    color:#111827;
}

.user{
    background:white;
    padding:12px 20px;
    border-radius:10px;
    box-shadow:0 2px 10px rgba(0,0,0,0.05);
}

/* CARDS */

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
    margin-bottom:30px;
}

.card{
    background:white;
    padding:30px;
    border-radius:15px;
    box-shadow:0 2px 10px rgba(0,0,0,0.05);
}

.card h3{
    color:gray;
    margin-bottom:10px;
}

.card h2{
    color:#16a34a;
    font-size:32px;
}

/* TABELA */

.table-box{
    background:white;
    padding:30px;
    border-radius:15px;
    box-shadow:0 2px 10px rgba(0,0,0,0.05);
}

.table-header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:20px;
}

.add-btn{
    background:#16a34a;
    color:white;
    border:none;
    padding:12px 18px;
    border-radius:10px;
    cursor:pointer;
}

table{
    width:100%;
    border-collapse:collapse;
}

table th{
    background:#f9fafb;
    padding:15px;
    text-align:left;
}

table td{
    padding:15px;
    border-bottom:1px solid #eee;
}

.edit{
    color:#16a34a;
    cursor:pointer;
    margin-right:10px;
}

.delete{
    color:red;
    cursor:pointer;
}

/* RESPONSIVO */

@media(max-width:900px){

    .sidebar{
        width:90px;
    }

    .sidebar .logo h2{
        display:none;
    }

    .menu a span{
        display:none;
    }

    .main{
        margin-left:90px;
    }

}

</style>

</head>
<body>

<!-- LOGIN -->

<div class="login-screen" id="loginScreen">

    <div class="login-box">

        <div class="logo">
            <i class="fa-solid fa-cart-shopping"></i>
            <h1>Mercadinho Seu Zé</h1>
            <p>Sistema de gerenciamento</p>
        </div>

        <div class="input-group">
            <i class="fa-solid fa-user"></i>
            <input type="text" placeholder="Usuário">
        </div>

        <div class="input-group">
            <i class="fa-solid fa-lock"></i>
            <input type="password" placeholder="Senha">
        </div>

        <button class="login-btn" onclick="entrar()">
            Entrar
        </button>

    </div>

</div>

<!-- SISTEMA -->

<div class="system" id="system">

    <!-- MENU -->

    <div class="sidebar">

        <div class="logo">
            <i class="fa-solid fa-cart-shopping"></i>
            <h2>Seu Zé</h2>
        </div>

        <div class="menu">

            <a href="#">
                <i class="fa-solid fa-chart-line"></i>
                <span>Dashboard</span>
            </a>

            <a href="#">
                <i class="fa-solid fa-box"></i>
                <span>Estoque</span>
            </a>

            <a href="#">
                <i class="fa-solid fa-users"></i>
                <span>Fornecedores</span>
            </a>

            <a href="#">
                <i class="fa-solid fa-cash-register"></i>
                <span>Vendas</span>
            </a>

            <a href="#">
                <i class="fa-solid fa-chart-pie"></i>
                <span>Relatórios</span>
            </a>

        </div>

    </div>

    <!-- CONTEÚDO -->

    <div class="main">

        <div class="topbar">

            <h1>Dashboard</h1>

            <div class="user">
                Admin
            </div>

        </div>

        <!-- CARDS -->

        <div class="cards">

            <div class="card">
                <h3>Produtos</h3>
                <h2>1248</h2>
            </div>

            <div class="card">
                <h3>Faturamento</h3>
                <h2>R$ 28.650</h2>
            </div>

            <div class="card">
                <h3>Vendas</h3>
                <h2>328</h2>
            </div>

            <div class="card">
                <h3>Clientes</h3>
                <h2>842</h2>
            </div>

        </div>

        <!-- TABELA -->

        <div class="table-box">

            <div class="table-header">

                <h2>Produtos em estoque</h2>

                <button class="add-btn">
                    + Novo Produto
                </button>

            </div>

            <table>

                <thead>

                    <tr>
                        <th>Produto</th>
                        <th>Categoria</th>
                        <th>Quantidade</th>
                        <th>Preço</th>
                        <th>Ações</th>
                    </tr>

                </thead>

                <tbody>

                    <tr>
                        <td>Arroz 5kg</td>
                        <td>Alimentos</td>
                        <td>50</td>
                        <td>R$ 23,90</td>

                        <td>
                            <i class="fa-solid fa-pen edit"></i>
                            <i class="fa-solid fa-trash delete"></i>
                        </td>
                    </tr>

                    <tr>
                        <td>Coca-Cola 2L</td>
                        <td>Bebidas</td>
                        <td>28</td>
                        <td>R$ 9,49</td>

                        <td>
                            <i class="fa-solid fa-pen edit"></i>
                            <i class="fa-solid fa-trash delete"></i>
                        </td>
                    </tr>

                    <tr>
                        <td>Papel Higiênico</td>
                        <td>Limpeza</td>
                        <td>20</td>
                        <td>R$ 16,90</td>

                        <td>
                            <i class="fa-solid fa-pen edit"></i>
                            <i class="fa-solid fa-trash delete"></i>
                        </td>
                    </tr>

                </tbody>

            </table>

        </div>

    </div>

</div>

<script>

function entrar(){

    document.getElementById('loginScreen').style.display = 'none';

    document.getElementById('system').style.display = 'block';

}

document.querySelectorAll('.edit').forEach(btn => {

    btn.addEventListener('click', () => {

        alert('Editar produto');

    });

});

document.querySelectorAll('.delete').forEach(btn => {

    btn.addEventListener('click', () => {

        let confirmar = confirm('Deseja excluir este produto?');

        if(confirmar){

            alert('Produto excluído');

        }

    });

});

</script>

</body>
</html>
