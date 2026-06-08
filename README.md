   Ferramentas que estão revolucionando o mercado.
                    </p>

                    <a href="#">Ler artigo →</a>
                </div>
            </article>

        </section>

    </main>

    <footer>
        <h3>TechBlog</h3>
        <p>© 2026 - Todos os direitos reservados.</p>
    </footer>

    <script src="script.js"></script>

</body>

</html>
style.css
:root{
    --bg:#0f172a;
    --card:#1e293b;
    --text:#f8fafc;
    --accent:#3b82f6;
}

.light{
    --bg:#f5f5f5;
    --card:#ffffff;
    --text:#111827;
    --accent:#2563eb;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    background:var(--bg);
    color:var(--text);
    transition:.4s;
}

header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:25px 10%;
    backdrop-filter:blur(15px);
    position:sticky;
    top:0;
    z-index:1000;
    background:rgba(15,23,42,.8);
}

.logo{
    font-size:1.7rem;
    font-weight:700;
    color:var(--accent);
}

nav a{
    color:var(--text);
    text-decoration:none;
    margin:0 15px;
    transition:.3s;
}

nav a:hover{
    color:var(--accent);
}

#theme-btn{
    background:none;
    border:none;
    color:white;
    font-size:1.4rem;
    cursor:pointer;
}

.hero{
    min-height:90vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:30px;
}

.hero-content{
    max-width:900px;
}

.tag{
    background:rgba(59,130,246,.15);
    color:#60a5fa;
    padding:10px 20px;
    border-radius:50px;
}

.hero h1{
    font-size:4rem;
    margin-top:25px;
    margin-bottom:20px;
}

.hero p{
    font-size:1.2rem;
    opacity:.8;
}

.hero-btn{
    display:inline-block;
    margin-top:30px;
    padding:15px 35px;
    background:var(--accent);
    color:white;
    text-decoration:none;
    border-radius:50px;
    transition:.3s;
}

.hero-btn:hover{
    transform:translateY(-5px);
}

.posts{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(350px,1fr));
    gap:30px;
    padding:80px 10%;
}

.card{
    background:var(--card);
    border-radius:20px;
    overflow:hidden;
    transition:.4s;
    box-shadow:0 10px 25px rgba(0,0,0,.2);
}

.card:hover{
    transform:translateY(-10px);
}

.card img{
    width:100%;
    height:250px;
    object-fit:cover;
}

.card-content{
    padding:25px;
}

.card-content span{
    color:#60a5fa;
}

.card-content h2{
    margin:15px 0;
}

.card-content p{
    opacity:.8;
}

.card-content a{
    display:inline-block;
    margin-top:20px;
    color:var(--accent);
    text-decoration:none;
}

footer{
    text-align:center;
    padding:40px;
    margin-top:50px;
    border-top:1px solid rgba(255,255,255,.1);
}

@media(max-width:768px){

    header{
        flex-direction:column;
        gap:20px;
    }

    .hero h1{
        font-size:2.5rem;
    }

}
script.js
const themeBtn = document.getElementById("theme-btn");

themeBtn.addEventListener("click", () => {

    document.body.classList.toggle("light");

    if(document.body.classList.contains("light")){
        themeBtn.textContent = "☀️";
    }else{
        themeBtn.textContent = "🌙";
    }

});
Estrutura do projeto
blog/
│
├── index.html
├── style.css
└── script.js
