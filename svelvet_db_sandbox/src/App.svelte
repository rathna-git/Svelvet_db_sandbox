<script>
  import {Svelvet, ThemeToggle} from 'svelvet';
  import Vessel from './lib/tables/Vessel.svelte';
  import People from './lib/tables/People.svelte';
  import Pilot from './lib/tables/Pilots.svelte';
  import Planet from './lib/tables/Planets.svelte';
  import Species from './lib/tables/Species.svelte';
  import Starship from './lib/tables/Starship_specs.svelte';
  import PeopleFilms from './lib/tables/People_in_films.svelte';
  import SpeciesFilms from './lib/tables/Species_in_films.svelte';
  import SpeciesInFilms from './lib/tables/Species_in_films.svelte';

</script>
<body>
  <Svelvet controls minimap >
    <Vessel/>
    <People/>
    <Pilot/>
    <Planet/>
    <Species/>
    <Starship/>
    <PeopleFilms/>
    <SpeciesInFilms/>
    <ThemeToggle main='light' alt='dark' slot='toggle'/>
  </Svelvet>
</body>

<style>
  body {
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: gray;
		width: 95vw;
		height: 95vh;
		padding: 0;
		margin: 0;
	}
</style>