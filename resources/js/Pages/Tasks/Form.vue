<template>
    <div class="sm:container mx-auto px-[5rem] py-10 mt-5 sm:max-w-6xl">
        <div>
            <div class="flex justify-center mb-8">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"
                     class="w-8 mr-3 text-yellow-500 fill-current">
                    <path
                        d="M256 0C114.6 0 0 114.6 0 256s114.6 256 256 256s256-114.6 256-256S397.4 0 256 0zM232 152C232 138.8 242.8 128 256 128s24 10.75 24 24v128c0 13.25-10.75 24-24 24S232 293.3 232 280V152zM256 400c-17.36 0-31.44-14.08-31.44-31.44c0-17.36 14.07-31.44 31.44-31.44s31.44 14.08 31.44 31.44C287.4 385.9 273.4 400 256 400z"/>
                </svg>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris dui diam, auctor sed placerat id,
                    egestas
                    a purus. Aliquam in orci sit amet magna mattis varius</p>
            </div>
            <div class="bg-white leading-[3rem] px-12 py-8 rounded-2xl mb-8">
                <p>
                    Liebe Claudia,
                    entschuldige, dass ich mich so lange nicht bei dir gemeldet
                    Wie du weißt, bin ich vor zwei Wochen
                    <draggable
                        class="dragArea list-group leading-[1rem]"
                        :list="list1"
                        group="people"
                        @change="log"
                        itemKey="name"
                    >
                        <template #item="{ element, index }">
                            <span class="list-group-item">
                                    <button class="text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                        </template>
                    </draggable>
                    Deswegen hatte ich leider keine Zeit <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list3"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> meine Freunde. Aber
                    deinen Vorschlag, mal wieder gemeinsam <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list4"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> Tag miteinander zu verbringen, finde ich sehr gut. Mir
                    passt
                    es auch am besten am Wochenende. Würde es bei dir schon <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list5"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> Samstag gehen? Da habe ich noch nichts
                    vor.
                    Es würde <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list6"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> natürlich freuen, wenn du dir bei dieser Gelegenheit auch meine neue Wohnung
                    anschaust. Es
                    ist wunderbar, so viel zu haben. Was meinst du, wir uns bei mir treffen und dann unsere Einkaufstour
                    machen? Oder ist es dir <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list7"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> , wenn wir zuerst einkaufen und am Abend zusammen kochen und essen?
                    Übrigens, können wir dein Auto nehmen? <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list8"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> steht schon wieder in der Werkstatt. Schreib mir doch
                    bald,
                    ob du an diesem Tag Zeit hast. <draggable
                    class="dragArea list-group leading-[1rem]"
                    :list="list9"
                    group="people"
                    @change="log"
                    itemKey="name"
                >
                    <template #item="{ element, index }">
                            <span class="list-group-item">
                                <button class="bg-white text-green-600 font-bold py-2 px-4 rounded border border-gray-400 min-w-[7rem]">
                                    {{ element.name }}
                                </button>
                            </span>
                    </template>
                </draggable> du keine Zeit hast, finden wir sicher einen anderen Tag.
                </p>
                <p class="mb-6">Marion</p>

                <hr class="mb-6 border-dashed">

                <draggable
                    class="dragArea1 list-group grid grid-cols-4 gap-4"
                    :list="list2"
                    group="people"
                    @change="log"
                    itemKey="name"
                >

                    <template #item="{ element, index }">
                        <span class="list-group-item">
                            <button class="bg-green-600 text-white font-bold leading-[1rem] py-2 px-4 rounded">
                                {{ element.name }}
                            </button>
                        </span>
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
    name: "two-lists",
    display: "Two Lists",
    order: 1,
    components: {
        draggable
    },

    watch: {
        list1: {
            handler() {
                if (this.list1.length > 1) {
                    this.list1 = this.list1.filter((list1) => list1.name !== '. . . .')
                }
            },
            deep: true
        },
        list3: {
            handler() {
                if (this.list3.length > 1) {
                    this.list3 = this.list3.filter((list3) => list3.name !== '. . . .')
                }
            },
            deep: true
        },
        list4: {
            handler() {
                if (this.list4.length > 1) {
                    this.list4 = this.list4.filter((list4) => list4.name !== '. . . .')
                }
            },
            deep: true
        },
        list5: {
            handler() {
                if (this.list5.length > 1) {
                    this.list5 = this.list5.filter((list5) => list5.name !== '. . . .')
                }
            },
            deep: true
        },
        list6: {
            handler() {
                if (this.list6.length > 1) {
                    this.list6 = this.list6.filter((list6) => list6.name !== '. . . .')
                }
            },
            deep: true
        },
        list7: {
            handler() {
                if (this.list7.length > 1) {
                    this.list7 = this.list7.filter((list7) => list7.name !== '. . . .')
                }
            },
            deep: true
        },
        list8: {
            handler() {
                if (this.list8.length > 1) {
                    this.list8 = this.list8.filter((list8) => list8.name !== '. . . .')
                }
            },
            deep: true
        },
        list9: {
            handler() {
                if (this.list9.length > 1) {
                    this.list9 = this.list9.filter((list9) => list9.name !== '. . . .')
                }
            },
            deep: true
        },
    },

    data() {
        return {
            list1: [
                {name: '. . . .', id: 1}
            ],
            list2: [
                {name: "umgezogen", id: 1},
                {name: "mich", id: 2},
                {name: "einen", id: 3},
                {name: "nächsten", id: 4},
                {name: "für", id: 5},
                {name: "lieber", id: 6},
                {name: "wollen", id: 7},
                {name: "Meines", id: 8}
            ],
            list3: [
                {name: '. . . .', id: 1},
            ],
            list4: [
                {name: '. . . .', id: 1},
            ],
            list5: [
                {name: '. . . .', id: 1},
            ],
            list6: [
                {name: '. . . .', id: 1},
            ],
            list7: [
                {name: '. . . .', id: 1},
            ],
            list8: [
                {name: '. . . .', id: 1},
            ],
            list9: [
                {name: '. . . .', id: 1},
            ],
            controlOnStart: true
        };
    },

    methods: {
        add: function () {
            this.list.push({name: "Juan"});
        },
        replace: function () {
            this.list = [{name: "Edgard"}];
        },
        clone: function (el) {
            return {
                name: el.name + " cloned"
            };
        },
        log: function (evt) {
            window.console.log(evt);
        }
    }
};
</script>
<style scoped>

</style>
