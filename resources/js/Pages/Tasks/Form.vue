<template>
    <div class="line flex">
        <div class="green-line"></div>
        <div class="green-lite-line w-full"></div>
    </div>
    <div class="bg-white min-h-[101px] flex justify-around items-center header">
        <p>Some Title</p>
        <button class="blue-btn">Nächste Frage</button>
    </div>

    <div class="sm:container mx-auto px-auto sm:max-w-6xl">

        <div class="flex justify-between items-center min-h-[158px]">
            <div>
                <div class="icon rounded-md flex items-center justify-center text-white">
                    <p class="font-bold">i</p>
                </div>
            </div>

            <div class="ml-6 min-h-[66px] flex items-center line-h">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris dui diam, auctor sed placerat id,
                egestas a purus. Aliquam in orci sit amet magna mattis varius
            </div>
        </div>

        <div class="bg-white leading-[3rem] px-12 py-8 rounded-2xl mb-8">
            <div>
                <div class="main-text">
                    Liebe Claudia,
                    entschuldige, dass ich mich so lange nicht bei dir gemeldet
                    Wie du weißt, bin ich vor zwei Wochen
                <div id="div1" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                Deswegen hatte ich leider keine Zeit .... meine Freunde.
                Aber deinen Vorschlag, mal wieder gemeinsam .... Tag miteinander zu verbringen, finde ich sehr gut.
                Mir passt es auch am besten am Wochenende. Würde es bei dir schon .... Samstag gehen? Da habe ich
                noch nichts vor. Es würde .... natürlich freuen, wenn du dir bei dieser Gelegenheit auch meine neue
                Wohnung anschaust. Es ist wunderbar, so viel zu haben. Was meinst du, wir uns bei mir treffen und
                dann unsere Einkaufstour machen? Oder ist es dir .... , wenn wir zuerst einkaufen und am Abend
                zusammen kochen und essen? Übrigens, können wir dein Auto nehmen? .... steht schon wieder in der
                Werkstatt. Schreib mir doch bald, ob du an diesem Tag Zeit hast. .... du keine Zeit hast, finden wir
                sicher einen anderen Tag.
                Marion
                </div>
            </div>

            <hr class="mb-6 border-dashed">

            <p id="drag1" draggable="true" @ondragstart="drag($event)">This is a draggable paragraph. Drag this element into the rectangle.</p>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        drop(ev) {
            let data = ev.dataTransfer.getData("Text");
            ev.target.appendChild(document.getElementById(data));
            ev.preventDefault();
        },
        allowDrop(ev) {
            ev.preventDefault();
        },
        drag(ev) {
            ev.dataTransfer.setData("Text", ev.target.id);
        }
    }
};
</script>
<style scoped>
.header {
    font-family: 'Archivo';
    font-style: normal;
    font-weight: 700;
    font-size: 28px;
    line-height: 45px;
    letter-spacing: 0.3px;
    color: #212831;
}

.blue-btn {
    background: #0872BA;
    border-radius: 8px;
    font-family: 'Archivo';
    font-style: normal;
    font-weight: 800;
    font-size: 20px;
    line-height: 22px;
    /* identical to box height */

    text-align: center;
    letter-spacing: 0.346154px;

    color: #FFFFFF;
    min-width: 196px;
    min-height: 60px;
}

.line {
    min-height: 8px;
}

.green-line {
    min-width: 189px;
    background-color: #1B998B;
}

.green-lite-line {
    background: rgba(27, 153, 139, 0.2);
}

.icon {
    width: 43px;
    height: 43px;
    background: #F3983F;
    font-size: 25px;
}
.line-h {
    line-height: 33px;
}
.main-text {
    line-height: 78px;
}
#div1 {
    width: 350px;
    height: 70px;
    padding: 10px;
    border: 1px solid #aaaaaa;
}
</style>
