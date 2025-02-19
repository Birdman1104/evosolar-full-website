<template>
    <section id="cases">
        <h2>Cases</h2>
        <p class="cases-description">Lorem ipsum dolor sit amet consectetur. Ipsum consequat ac egestas vestibulum
            integer vivamus ullamcorper
            ultrices. Proin eu at tortor eget. Semper sed mattis volutpat urna at congue. Nibh arcu proin iaculis
            odio.
            Ridiculus lorem sit facilisi.
        </p>
        <div class="cases-section">
            <div class="case" v-for="(block, index) in blocks" :key="index">
                <h3>{{ block.title }}</h3>
                <p>{{ block.text }}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            blocks: [
                { title: 'Service', units: ['XY unit', 'YY unit'] },
                { title: 'Service', units: ['XX unit', 'XY unit', 'YY unit'] },
                { title: 'Service', units: ['XX unit', 'XY unit', 'YY unit'] },
                { title: 'Service', units: ['XX unit', 'YY unit'] },
                { title: 'Service', units: ['XX unit', 'XY unit', 'YY unit'] },
            ],
        };
    },
};
</script>


<style scoped>
#cases {
    background: #04210c;
    padding: 20px;
}

#cases h2 {
    color: white;
    font-size: 2rem;
    text-align: center;
}

#cases p {
    color: white;
    font-size: 0.8rem;
    text-align: center;
    margin-bottom: 20px;
}

.cases-description {
    max-width: 800px;
    margin: 10 auto;
    font-size: 0.8rem;
    line-height: 1.6;
    font-weight: 100;
}

.cases-section {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto auto;
    gap: 10px;

}

.case:nth-child(4n-3),
.case:nth-child(4n) {
    grid-column: span 7;
}

.case:nth-child(4n-2),
.case:nth-child(4n-1) {
    grid-column: span 5;
}

.case {
    border: 5px solid #237878;
    padding: 20px;
    color: white;
}

.case:only-child,
.case:last-child:nth-child(4n-3) {
    grid-column: span 12;
}

@media (max-width: 768px) {
    .cases-section {
        grid-template-columns: 1fr;
        grid-template-rows: repeat(4, auto);
    }

    .cases-section .case {
        grid-column: span 12;
    }
}
</style>