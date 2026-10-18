<script>
import '$lib/assets/stylesheet/global.css'
import '$lib/assets/stylesheet/layout.css'
import Button from "$component/Button"
</script>

<div class="landing-page">
    <div id="landing-page-text">
        <h1>Anvesha</h1>
        <h2>A one place platform where NCERT-based education resources are visualised in 3D.</h2>
        <Button href="about">Learn More</Button>
    </div>

    <div id="login-div">
        <Button>Login</Button>
        <Button>Sign Up</Button>
        <!-- <div id="login-credentials">
            <p>Username: </p>
            <input type="text" placeholder="Username">
            <p>Password: </p>
            <input type="password" placeholder="Password">
            <Button>Login</Button>
        </div> -->

        <div id="signup-credentials">
            <p>Username:</p>
            <input type="text" placeholder="Username">
            <p>Password: </p>
            <input type="password" placeholder="Password">
            <p>Confirm Password: </p>
            <input type="password" placeholder="Confirm Password">
            <p>Email: </p>
            <input type="email" placeholder="Email">
            <Button>Sign Up</Button>
        </div>

    </div>

</div>