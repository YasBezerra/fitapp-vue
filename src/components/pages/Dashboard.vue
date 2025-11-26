<script setup>
    import Grid from '../Grid.vue'
    import { gymHealthFacts } from '../../utils';
    const randomNumber = Math.floor(Math.random() * gymHealthFacts.length)
    const todaysFact = gymHealthFacts[randomNumber]
    
    
</script>

<template>
  <section id="dashboard">
    <div class="card tip-container">
        <h2>Welcome Smoldier</h2>
        <div>
            <p class="tip"><strong>Daily tip</strong><br/>{{ todaysFact }}</p>
        </div>
        <div>
        <button>Start Workout &rarr;</button>
    </div>
    </div>
    <Grid/>
  </section>
</template>

<style scoped>
    .tip-container,
    .tip-container div,
    #dashboard {
        display: flex;
    }

    .tip-container,
    #dashboard {
        flex-direction: column;
    }

    #dashboard{
        gap: 2rem;
    }

    .tip-container {
        gap: 0.5rem;
    }

    @media (min-width: 640px){
        .tip-container{
            gap: 1rem;
        }
    }

</style>
