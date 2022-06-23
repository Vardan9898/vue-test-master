<template>
    <div class="sm:container mx-auto px-[5rem] py-10 mt-5 sm:max-w-6xl">
        <div>
            <div class="flex justify-center mb-8">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="w-8 mr-3">
                    <path
                        d="M256 0C114.6 0 0 114.6 0 256s114.6 256 256 256s256-114.6 256-256S397.4 0 256 0zM232 152C232 138.8 242.8 128 256 128s24 10.75 24 24v128c0 13.25-10.75 24-24 24S232 293.3 232 280V152zM256 400c-17.36 0-31.44-14.08-31.44-31.44c0-17.36 14.07-31.44 31.44-31.44s31.44 14.08 31.44 31.44C287.4 385.9 273.4 400 256 400z"/>
                </svg>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris dui diam, auctor sed placerat id,
                    egestas
                    a purus. Aliquam in orci sit amet magna mattis varius</p>
            </div>
            <div class="bg-white leading-[3rem] px-12 py-8 rounded-2xl mb-8">
                <draggable
                    class="dragArea list-group"
                    :list="list1"
                    :clone="clone"
                    :group="{ name: 'people', pull: pullFunction }"
                    @start="start"
                    item-key="id"
                >
                    <template #item="{ element }">
                        <div class="list-group-item">
                            <button class="bg-green-600 text-white font-bold py-2 px-4 rounded">
                                {{ element.name }}
                            </button>
                        </div>
                    </template>
                </draggable>
                <p>
                    Liebe Claudia,
                    entschuldige, dass ich mich so lange nicht bei dir gemeldet
                    Wie du weißt, bin ich vor zwei Wochen .... Deswegen hatte ich leider keine Zeit .... meine Freunde. Aber
                    deinen Vorschlag, mal wieder gemeinsam .... Tag miteinander zu verbringen, finde ich sehr gut. Mir passt
                    es auch am besten am Wochenende. Würde es bei dir schon .... Samstag gehen? Da habe ich noch nichts vor.
                    Es würde .... natürlich freuen, wenn du dir bei dieser Gelegenheit auch meine neue Wohnung anschaust. Es
                    ist wunderbar, so viel zu haben. Was meinst du, wir uns bei mir treffen und dann unsere Einkaufstour
                    machen? Oder ist es dir .... , wenn wir zuerst einkaufen und am Abend zusammen kochen und essen?
                    Übrigens, können wir dein Auto nehmen? .... steht schon wieder in der Werkstatt. Schreib mir doch bald,
                    ob du an diesem Tag Zeit hast. .... du keine Zeit hast, finden wir sicher einen anderen Tag.
                </p>
                <p class="mb-6">Marion</p>

                <hr class="mb-6 border-dashed">

                    <draggable
                        class="dragArea list-group grid grid-cols-4 gap-4"
                        :list="list2"
                        group="people"
                        item-key="id"
                    >
                        <template #item="{ element }">
                                <div class="list-group-item">
                                    <button class="bg-green-600 text-white font-bold py-2 px-4 rounded">
                                        {{ element.name }}
                                    </button>
                                </div>
                        </template>
                    </draggable>
            </div>
        </div>
    </div>
</template>

<script>
import draggable from "vuedraggable";
let idGlobal = 8;
export default {
    name: "clone-on-control",
    display: "Clone on Control",
    instruction: "Press Ctrl to clone element from list 1",
    order: 4,
    components: {
        draggable
    },
    data() {
        return {
            list1: [
                { name: "draggable 1", id: 1 },
            ],
            list2: [
                { name: "umgezogen", id: 1 },
                { name: "mich", id: 2 },
                { name: "einen", id: 3 },
                { name: "nächsten", id: 4 },
                { name: "für", id: 5 },
                { name: "lieber", id: 6 },
                { name: "wollen", id: 7 },
                { name: "Meines", id: 8 }
            ],
            controlOnStart: true
        };
    },
    methods: {
        clone({ name }) {
            return { name, id: idGlobal++ };
        },
        pullFunction() {
            return this.controlOnStart ? "clone" : true;
        },
        start({ originalEvent }) {
            this.controlOnStart = originalEvent.ctrlKey;
        }
    }
};
</script>
<style scoped></style>
<!--<template>-->
<!--    <div class="row">-->
<!--        <div class="col-3">-->
<!--            <h3>Draggable 1</h3>-->
<!--            <draggable-->
<!--                class="dragArea list-group"-->
<!--                :list="list1"-->
<!--                :group="{ name: 'people', pull: 'clone', put: false }"-->
<!--                :clone="cloneDog"-->
<!--                @change="log"-->
<!--                item-key="id"-->
<!--            >-->
<!--                <template #item="{ element }">-->
<!--                    <div class="list-group-item">-->
<!--                        {{ element.name }}-->
<!--                    </div>-->
<!--                </template>-->
<!--            </draggable>-->
<!--        </div>-->

<!--        <div class="col-3">-->
<!--            <h3>Draggable 2</h3>-->
<!--            <draggable-->
<!--                class="dragArea list-group"-->
<!--                :list="list2"-->
<!--                group="people"-->
<!--                @change="log"-->
<!--                item-key="id"-->
<!--            >-->
<!--                <template #item="{ element }">-->
<!--                    <div class="list-group-item">-->
<!--                        {{ element.name }}-->
<!--                    </div>-->
<!--                </template>-->
<!--            </draggable>-->
<!--        </div>-->

<!--&lt;!&ndash;        <rawDisplayer class="col-3" :value="list1" title="List 1" />&ndash;&gt;-->

<!--&lt;!&ndash;        <rawDisplayer class="col-3" :value="list2" title="List 2" />&ndash;&gt;-->
<!--    </div>-->
<!--</template>-->

<!--<script>-->
<!--import draggable from "vuedraggable";-->
<!--// import {list} from "postcss";-->
<!--// import RawDisplayer from "../../components/infra/raw-displayer";-->

<!--let idGlobal = 8;-->
<!--export default {-->
<!--    name: "custom-clone",-->
<!--    display: "Custom Clone",-->
<!--    order: 3,-->
<!--    components: {-->
<!--        draggable,-->
<!--        // RawDisplayer-->
<!--    },-->
<!--    data() {-->
<!--        return {-->
<!--            list1: [-->
<!--                { name: "umgezogen", id: 1 },-->
<!--                { name: "mich", id: 2 },-->
<!--                { name: "einen", id: 3 },-->
<!--                { name: "nächsten", id: 4 },-->
<!--                { name: "für", id: 5 },-->
<!--                { name: "lieber", id: 6 },-->
<!--                { name: "wollen", id: 7 },-->
<!--                { name: "Meines", id: 8 }-->
<!--            ],-->
<!--            list2: [-->
<!--                { name: 's', id: 5 }-->
<!--            ]-->
<!--        };-->
<!--    },-->
<!--    methods: {-->
<!--        log: function(evt) {-->
<!--            window.console.log(evt);-->
<!--        },-->
<!--        cloneDog({ name }) {-->
<!--            return {-->
<!--                id: idGlobal++,-->
<!--                name: `${name}`-->
<!--            };-->
<!--        }-->
<!--    }-->
<!--};-->
<!--</script>-->
<!--<style scoped></style>-->
