<div class="logo-header">
    <img src="../src/media/logo.gif" alt="Mas que papel logo" style="width: 25vw; display: inline-block;">
    <h1 style="display:inline-block;">Bokhandel</h1>
</div>
<nav>
    <a href="#anbefalt">Anbefalte bøker</a>
    <a href="#japansk">Japanske bøker</a>
    <a href="#andeby">Andeby</a>
    <a href="#eupåen">Europeisk på engelsk</a>
</nav>

<svelte:body />

<style>
	:global(body) {
		margin: 0;
	}

    .logo-header{
    display: flex;
    align-items: center;
    vertical-align: middle;
    }

    nav{
        display: flex;
        flex-wrap: nowrap;
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

</style>