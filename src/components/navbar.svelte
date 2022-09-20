<script>
    // THIS SHIT DONT WORK LMAO

    // let hideNavbar = false
    // function toggleNavbar() {
    //     let navElem = document.querySelector("nav")
    //     if (hideNavbar == true) {
    //         navElem.style.display = "none"
    //         hideNavbar = false
    //     }
    //     else if (hideNavbar == false){
    //         navElem.style.display = "flex"
    //         hideNavbar = true
    //     }
    // }
</script>

<div class="logo-header">
    <img src="logo.gif" alt="Mas que papel logo" style="width: 20vw; display: inline-block;">
    <h1 style="display:inline-block;">Bokhandel</h1>

    <!-- <div style="display: flex; justify-content:flex-end; width:100%; margin-right:15px;">
        <button on:click="{toggleNavbar()}">
            <svg viewBox="0 0 75 40" width="40" height="40">
                <rect width="75" height="10"></rect>
                <rect y="20" width="75" height="10"></rect>
                <rect y="40" width="75" height="10"></rect>
            </svg>
        </button>
    </div> -->
</div>

<nav>
    <a href="#Anbefalt!">Anbefalte bøker</a>
    <a href="#Japansk">Japanske bøker</a>
    <a href="#andeby">Andeby</a>
    <a href="#eupåen">Europeisk på engelsk</a>
</nav>

<style>
    .logo-header{
        display: flex;
        align-items: center;
        margin: 5px;
    }
    .logo-header:last-child{
        justify-content: flex-end;
    }

    nav{
        display: flex;
        flex-wrap: nowrap;
        flex-direction: row;
        justify-content: space-around;

        box-shadow: 0 2px 5px 0 rgb(0 0 0 / 16%), 0 2px 10px 0 rgb(0 0 0 / 12%);
    }
    nav a{
        flex: 1;
        text-align: center;
        padding: 15px;
        text-decoration: none;
        font-size: larger;
        color: black;
        transition-duration: 2s;
    }
    nav a:not(:last-child){
        border-right: 1px solid rgb(0 0 0 / 16%);
    }
    nav a:hover{
        background-color: rgba(128, 190, 210, 0.503);
        flex:2;
    }

    /* Media queries */
    @media screen and (min-width: 550px) and (max-width: 900px) {
		nav {
            font-size: 75%;
		}
	}
	@media screen and (max-width: 550px) {
		nav {
            flex-direction: column;
			grid-template-columns: 85%;
			row-gap: 1rem;
		}
	}
</style>