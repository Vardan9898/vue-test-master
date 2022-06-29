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
                    Deswegen hatte ich leider keine Zeit
                    <div class="droptarget area inline-block relative" @ondrop="drop($event)" @ondragover="allowDrop($event)">
<!--                        <button id="x-button" class="x-button absolute hidden"></button>-->
                    </div>
                    meine Freunde.
                    Aber deinen Vorschlag, mal wieder gemeinsam
                    <div class="droptarget area inline-block" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                    Tag miteinander zu verbringen, finde ich sehr gut.
                    Mir passt es auch am besten am Wochenende. Würde es bei dir schon
                    <div class="droptarget area inline-block" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                    Samstag gehen? Da habe ich
                    noch nichts vor. Es würde
                    <div class="droptarget area inline-block" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                    natürlich freuen, wenn du dir bei dieser Gelegenheit auch meine neue
                    Wohnung anschaust. Es ist wunderbar, so viel zu haben. Was meinst du, wir uns bei mir treffen und
                    dann unsere Einkaufstour machen? Oder ist es dir
                    <div class="droptarget area inline-block" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                    , wenn wir zuerst einkaufen und am Abend
                    zusammen kochen und essen? Übrigens, können wir dein Auto nehmen?
                    <div class="droptarget area inline-block" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                    steht schon wieder in der
                    Werkstatt. Schreib mir doch bald, ob du an diesem Tag Zeit hast.
                    <div class="droptarget area inline-block" @ondrop="drop($event)" @ondragover="allowDrop($event)"></div>
                    du keine Zeit hast, finden wir
                    sicher einen anderen Tag.
                    Marion
                </div>
            </div>

            <hr class="mb-6 border-dashed">

            <div class="grid grid-cols-4 gap-4">
                <div class="droptarget area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget">umgezogen</p>
                </div>
                <div class="droptarget1 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget1">mich</p>
                </div>
                <div class="droptarget2 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget2">einen</p>
                </div>
                <div class="droptarget3 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget3">nächsten</p>
                </div>
                <div class="droptarget4 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget4">für</p>
                </div>
                <div class="droptarget5 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget5">lieber</p>
                </div>
                <div class="droptarget6 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget6">wollen</p>
                </div>
                <div class="droptarget7 area justify-items-center" @ondrop="drop($event)" @ondragover="allowDrop($event)">
                    <p class="flex justify-center" @ondragstart="dragStart($event)" draggable="true" id="dragtarget7">Meines</p>
                </div>
            </div>


            <p id="demo"></p>

        </div>
    </div>
</template>

<script>
document.addEventListener("dragstart", function (event) {
    event.dataTransfer.setData("Text", event.target.id);
    document.getElementById("demo").innerHTML = "Started to drag the p element.";
});

document.addEventListener("dragover", function (event) {
    event.preventDefault();
});

document.addEventListener("drop", function (event) {
    event.preventDefault();
    let data = event.dataTransfer.getData("Text");
    event.target.appendChild(document.getElementById(data));
    document.getElementById("demo").innerHTML = "The p element was dropped";
    document.getElementById('x-button').classList.remove('hidden');
    document.getAttribute('draggable')
});

export default {
    methods: {}
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

.area {
    height: 46px;
    width: 189px;
    border-radius: 10px;
    background: #FFFFFF;
    border: 1px solid rgba(0, 0, 0, 0.15);
}

.x-button {
    height: 29px;
    width: 29px;
    left: 90%;
    top: -36%;
    background: #E83F6F;
    border: 1px solid #E83F6F;
    border-radius: 50%;
}
</style>
