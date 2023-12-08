<script>
	import { onMount } from "svelte";

	onMount(() => {
    console.log("hoi")

      let kanCirkelTekenen = true;

      function tekenGekleurdeCirkel(event) {
        if (kanCirkelTekenen) {
          const kleuren = ['#ffd6e8', '#ffbdda', '#e89898'];
          const willekeurigeKleur = kleuren[Math.floor(Math.random() * kleuren.length)];

          const cirkel = document.createElement('div');
          cirkel.className = 'cirkel';
          cirkel.style.backgroundColor = willekeurigeKleur;

          const x = event.clientX;
          const y = event.clientY;

          cirkel.style.left = `${x - 5}px`;
          cirkel.style.top = `${y - 5}px`;

          document.body.appendChild(cirkel);

          kanCirkelTekenen = false;

          // Interfall time
          setTimeout(() => {
            document.body.removeChild(cirkel);
            kanCirkelTekenen = true;
          }, 1800);
        }
      }

      document.addEventListener('mousemove', tekenGekleurdeCirkel);
    });
 
</script>