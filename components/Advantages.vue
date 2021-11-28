<template>
  <div class="advantages-wrapper">
    <Advantage
      v-for="(advantage, itemObjKey) in advantages"
      :key="itemObjKey + 1"
      :advantage="advantage"
    />
  </div>
</template>

<script>
export default {
  data: () => ({
    advantages: [
      {
        title: 'Résilience et maintien',
        img: require('../assets/images/advantage1.svg'),
        desc: "Nos matelas s'adaptent au dormeur et non l'inverse",
      },
      {
        title: 'Matières naturelles',
        img: require('../assets/images/advantage2.svg'),
        desc: 'Nos matelas sont extrêments respirants, déhoussables, anti acariens et antibactériens',
      },
      {
        title: 'Economiques et écologique',
        img: require('../assets/images/advantage3.svg'),
        desc: 'Des coûts optimisés grâce à une durée de vie double',
      },
      {
        title: 'Prix réduits',
        img: require('../assets/images/advantage4.svg'),
        desc: 'Des tarifs professionnels avantageux',
      },
      {
        title: 'Un chargé de compte dédié',
        img: require('../assets/images/advantage5.svg'),
        desc: 'Un accompagnement marketing sur-mesure',
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.advantages-wrapper {
  display: flex;
  justify-content: space-between;
  justify-content: center;
  align-items: center;
  margin: 40px 0;
}
</style>
