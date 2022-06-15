<script>
    import Nav from '../components/Common/Nav.svelte'
    import Footer from '../components/Common/Footer.svelte'
    import '../app.css'
</script>

<div>
    <Nav />
    <slot></slot>
    <Footer />
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500&display=swap');
    
    * {
        font-family: 'Space Grotesk', sans-serif;
        box-sizing: border-box;
        margin: 0;
        padding: 0;
        overflow: hidden;
    }
</style>
