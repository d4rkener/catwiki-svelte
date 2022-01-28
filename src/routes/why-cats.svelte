<script>
  const whyCatsPoints = [
    {
      id: 1,
      title: "1. They're hilarious",
      description:
        'They really are. From their random dances and leaps, to their fascination with a speck of dust, cats provide a regular source of amusing entertainment. Need proof? Just search for funny cat videos online.'
    },
    {
      id: 2,
      title: '2. They show you that anything can be a bed',
      description:
        'A washbasin, an impossibly small box, a computer keyboard, even a sheet of paper on the floor. A cat shows you that there are no limits to what can be used as a bed.'
    },
    {
      id: 3,
      title: '3. They keep you grounded',
      description:
        'If you ever start to become too full of your own self-importance, a swift derisive look from your cat will be enough to remind you that you’re not as awesome as you think you are.'
    },
    {
      id: 4,
      title: "4. They're great company",
      description:
        'They pretty much just want to hang out and relax, eat a little, play a little, snuggle a little - the perfect companion. '
    },
    {
      id: 5,
      title: "5. They're loving",
      description:
        "Sure it's on their terms, and only when they want it, but when they decide it's time to allow you to pet them, you will be rewarded with warmth and affection that melts your heart."
    },
    {
      id: 6,
      title: '6. They bring you gifts',
      description:
        'A half-chewed mouse might not be at the top of your desired gift list, but you can at least appreciate the sentiment.'
    },
    {
      id: 7,
      title: "7. They don't mind if you give them silly names",
      description:
        "They really don't, so indulge your crazy name fantasies on them. Just remember, though, that this is the name you will have to answer to when they call it out at the vet office."
    },
    {
      id: 8,
      title: "8. They're cute, really cute",
      description:
        "Seriously, why wouldn't you want something fluffy and cute walking around your home? Just observing their day-to-day routine is enough to fill your heart."
    },
    {
      id: 9,
      title: '9. Their purring is beneficial to humans',
      description:
        'There has actually been some research showing that the sound frequency at which a cat purrs can have potentially healing health benefits for you. Whether or not this is proven, any cat owner knows that the sound of that purr often helps their feelings of stress and anxiety melt away.'
    },
    {
      id: 10,
      title: '10. They have good bathroom habits',
      description:
        'In general, cats keep themselves meticulously clean, and always use the littler box, or even the neighbor’s yard, to do their toilet business.'
    }
  ];
</script>

<svelte:head>
  <title>CatWiki | Why Should You Have A Cat?</title>
</svelte:head>

<div class="why-cats">
  <h1 class="why-cats__heading">Why should you have a cat?</h1>
  {#each whyCatsPoints as point (point.id)}
    <div class="why-cats__point">
      <h3>{point.title}</h3>
      <p>{point.description}</p>
    </div>
  {/each}
</div>

<style lang="scss">
  @use '../scss/_variables.scss' as var;
  @use '../scss/_breakpoints.scss' as md;

  .why-cats {
    &__heading {
      font-size: 2.5rem;
      color: var.$cannonBlack;
      margin-bottom: 1.25rem;

      @include md.breakpoint(large) {
        font-size: 3rem;
      }
    }

    &__point {
      &:not(:last-child) {
        margin-bottom: 1.25rem;
      }

      h3 {
        font-size: 1.5rem;
        color: var.$cannonBlack;
        font-weight: 600;

        @include md.breakpoint(medium) {
          font-size: 1.875rem;
        }
      }

      p {
        margin-top: 0.625rem;

        @include md.breakpoint(medium) {
          font-size: 1.125rem;
        }
      }
    }
  }
</style>
