<!----<template>

    <header>
        <div>
            <RouterLink to="/">
                <h1 class="homeTitle">Ewin</h1>
            </RouterLink>
            </div>
            <div>
            <RouterLink to="/">Home</RouterLink> &gt; Sign up
        </div>
    </header>

    <main>
        <h2>Sign up</h2>
        <form  method="post" class="memberForm"> Formulaire de connection
            <label> Username <br />
                <input type="text" id="username" name="username" placeholder="Username" required autofocus>
            </label><br />
            <label> Email <br />
                <input type="email" id="email" name="email" placeholder="Email" required autofocus>
            </label><br />
            <label> Password <br />
                <input type="password" id="password" name="password" placeholder="Password" required>
            </label><br />
            <input type="submit" value="Connexion" class="memberSubmit">
        </form>

        <div class="linkSignup"> Contient les liens de naviguations
            <div>
                Already have an account ? <RouterLink to="/signin">Sign in</RouterLink>
            </div>
        </div>
  </main>

</template> -->

<template>

  <header>
    <div>
      <RouterLink to="/">
        <h1 class="homeTitle">Ewin</h1>
      </RouterLink>
    </div>
    <div>
      <RouterLink class="link" to="/">Home</RouterLink> &gt; Sign up
    </div>
  </header>

  <main>
    <div class="formContainer">
      <h2>Sign up</h2>
      <form  method="post" class="memberForm"> <!--Formulaire de connection-->

        <label for="username">Username</label>
        <input type="text" id="username" name="username" required autofocus> <br />

        <label for="email">Email</label>
        <input type="email" id="email" name="email" required> <br />

        <label for="password">Password</label>
        <input type="password" id="password" name="password" required> <br />

        <label for="password">Password verification</label>
        <input type="password" id="passwordVerif" name="passwordVerif" required> <br />

        <input type="submit" value="Connexion" class="memberSubmit">
      </form>

      <div class="linkSignin"> <!--Contient les liens de naviguations-->
        <div>
          You alreay have an account ? <RouterLink class="link" to="/signin">Sign in</RouterLink>
        </div>
      </div>
    </div>
    
  </main>

</template>

<!--<style scoped>

  main{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin:0;

    /*background: linear-gradient(
      100deg,
      #08D9D6,
      #e668d1,
      #08D9D6,
      #ff2e63

    );
    height: 100vh;
    background-size:400% 400%;
    animation: gradient 15s ease-in infinite;*/
  }

  /*@keyframes gradient {
    0% {
      background-position: 0% 0%;
    }
    50% {
      background-position: 100% 100%;
    }
    100% {
      background-position: 0% 0%;
    }
  }*/

  h1{
    font-size: 3em;
    font-weight: bold;
  }

  h2{
    font-size: 2em;
  }

  header{
    margin-left:4em;
    margin-top:1.5em;
  }

  .linkSignup{
    display: flex;
    justify-content: center;
    width: 400px;
    align-items: center;
    margin-top: 1em;
  }

  .memberForm{
    background-color: #393E46;
    padding:20px 20px 10px 20px;
    border-radius: 0.5em;
    margin-top: 1em;
    margin-bottom: 1em;
    border: solid #00ADB5 1px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
  }

  input[type=submit]:hover{
    cursor: pointer ;
  }

  input:not(#searchBar, .memberSubmit, :read-only), select{
    border: solid rgba(128, 128, 128, 0.15) 0.08em;
    color : #EEEEEE;
    border-bottom-color: #00ADB5;
    width: 11em;
    font-size: 1.15em;
    margin-bottom: 1em;
    margin-top:0.7em;
    border-radius: 0.2em;
    background-color: #222831;
    padding: 0.2em 0 0.2em 0.2em;
  }

  input[type=text]:read-only {
    border: solid rgba(128, 128, 128, 0.15) 0.08em;
    color : #EEEEEE;
    border-bottom-color:#00ADB5;
    font-size: 1.15em;
    margin-bottom: 1em;
    margin-top:0.7em;
    border-radius: 0.2em;
    background-color: #222831;
    padding: 0.2em 0 0.2em 0.2em;
  }

  input:focus{
    outline: none;
  }

  .memberSubmit{
    font-size: 1.15em;
    width: 11em;
    color: #EEEEEE;
    background-color: hsla(160, 100%, 37%, 1);
    border: solid rgba(128, 128, 128, 0.15) 0.08em;
    border-radius: 0.2em;
    margin-bottom: 0.8em;
    margin-top:0.5em;
  }
</style> -->

<style scoped>

  main{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin:0;

    /*background: linear-gradient(
      100deg,
      #08D9D6,
      #e668d1,
      #08D9D6,
      #ff2e63

    );
    height: 100vh;
    background-size:400% 400%;
    animation: gradient 15s ease-in infinite;*/
  }

  /*@keyframes gradient {
    0% {
      background-position: 0% 0%;
    }
    50% {
      background-position: 100% 100%;
    }
    100% {
      background-position: 0% 0%;
    }
  }*/

  h1{
    font-size: 3em;
    font-weight: bold;
    color:hsla(160, 100%, 37%, 1);
  }

  h2{
    font-size: 2em;
  }

  header{
    margin-left:4em;
    margin-top:1.5em;
  }

  .linkSignin{
    display: flex;
    justify-content: center;
    width: 400px;
    align-items: center;
    margin-top: 1em;
  }

  .formContainer{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 2em;
    background-color: #393E46;
    border-radius: 0.5em;
    border: #20242c solid 1px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    width: 30vw;
    height: 75vh;
    padding-top: 2em;
  }

  .memberForm{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    margin-top: 1em;
    width: 100%;
    height: 80%;
  }

  label{
    width: 100%;
    padding-left: 1.3em;
    margin-bottom: 0.5em;
    font-size: 1.2em;
    color: #EEEEEE;
  }

  input:not([type=submit]){
    width: 90%;
    font-size: 1em;
    height: 7.8%;
    border-radius: 0.4em;
    border: none;
    background-color: #20242c;
    color: #EEEEEE;
    
    padding: 0.2em 0 0.2em 0.8em;
  }

  input[type=submit]{
    width: 90%;
    font-size: 1em;
    height: 7.8%;
    border-radius: 0.4em;
    margin-top: 1em;
    background-color: #EEEEEE;
    color: #393E46;
    border: hsla(160, 0%, 100%, 0.5) solid 1px;
    cursor: pointer; 
  }

  input:focus{
    outline: none;
    box-shadow: 0 0 0 3px hsla(160, 100%, 37%, 0.5), 0 0 0 3px hsla(160, 100%, 37%, 0.5);
    /*border: hsla(160, 100%, 37%, 0.5) 1px solid;*/
  }

  /*.memberForm{
    background-color: #393E46;
    padding:20px 20px 10px 20px;
    border-radius: 0.5em;
    margin-top: 1em;
    margin-bottom: 1em;
    border: solid #00ADB5 1px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
  }*/

  .passwordForgot{
    color: #EEEEEE;
    cursor: pointer;
  }

  /*input[type=submit]:hover{
    cursor: pointer ;
  }

  input:not(#searchBar, .memberSubmit, :read-only), select{
    border: solid rgba(128, 128, 128, 0.15) 0.08em;
    color : #EEEEEE;
    border-bottom-color: #00ADB5;
    width: 11em;
    font-size: 1.15em;
    margin-bottom: 1em;
    margin-top:0.7em;
    border-radius: 0.2em;
    background-color: #222831;
    padding: 0.2em 0 0.2em 0.2em;
  }

  input[type=text]:read-only {
    border: solid rgba(128, 128, 128, 0.15) 0.08em;
    color : #EEEEEE;
    border-bottom-color:#00ADB5;
    font-size: 1.15em;
    margin-bottom: 1em;
    margin-top:0.7em;
    border-radius: 0.2em;
    background-color: #222831;
    padding: 0.2em 0 0.2em 0.2em;
  }

  input:focus{
    outline: none;
  }

  .memberSubmit{
    font-size: 1.15em;
    width: 11em;
    color: #EEEEEE;
    background-color: hsla(160, 100%, 37%, 1);
    border: solid rgba(128, 128, 128, 0.15) 0.08em;
    border-radius: 0.2em;
    margin-bottom: 0.8em;
    margin-top:0.5em;
  }*/
</style>