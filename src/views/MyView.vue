
<script>

import SingleComponent from '../components/myComponents/SingleComponent.vue';
import RawHtmlData from '../components/myComponents/RawHtmlData.vue';
import DirectiveVShow from '../components/myComponents/directives/DirectiveVShow.vue';
import DirectiveVIf from '../components/myComponents/directives/DirectiveVIf.vue';
import DirectiveVModel from '../components/myComponents/directives/DirectiveVModel.vue';
import DirectiveVFor from '../components/myComponents/directives/DirectiveVFor.vue';
import ParentComponent from '../components/myComponents/props/ParentComponent.vue';
import ComputedProps from '../components/myComponents/computed-properties/ComputedProps.vue';


export default { components: { SingleComponent, RawHtmlData, DirectiveVShow, DirectiveVIf, DirectiveVModel, DirectiveVFor, ParentComponent, ComputedProps, } };


/* export default { components: { SingleComponent } }; */
</script>

<template>
    <div>
        <h1>Hello Vue</h1>
<!--         <h3>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vero illum deserunt consequuntur repellat odit. Placeat iusto hic qui, totam, unde nam mollitia et suscipit ipsam quibusdam quo facilis repellendus ut?</h3>
 -->        ---------------------------
        <RawHtmlData />
        ---------------------------
        <SingleComponent />
        ---------------------------
        <DirectiveVShow />
        <DirectiveVIf />
        ---------------------------
        <DirectiveVModel />
        ---------------------------
        <DirectiveVFor />
        ---------------------------
        <computed-props />
        ---------------------------
        <parent-component></parent-component>

        

    </div>
</template>

<style lang="css" scoped>
h1 {
    color: rgb(118, 118, 190);
}
</style>