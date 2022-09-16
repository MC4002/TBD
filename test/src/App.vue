<template>
<div>
    <h1>Music Note Sightreading</h1>
    <h2>Treble and Bass Clef</h2>
    <Card class="Card"
    v-for="Note in Notes"
    :key="Note.NoteName"
    :Clef="Note.Clef"
    :Image="Note.Img"> 
    </Card>
</div>
</template>

<script>
import Card from './components/icons/Card.vue';

export default {
    name: "TBD",
    components: { Card },
    data () {
        return {
            Scale: "https://th.bing.com/th/id/R.4c9136e2c6df028d3eccaf398fa2cd29?rik=uYxj7Y5dnSTKWw&riu=http%3a%2f%2fbagha.ca%2fwp-content%2fuploads%2f2015%2f07%2fpiano3-small.png&ehk=L%2f3sy6TWG%2fFflU5rYmw8snStzxSFadv%2bAP%2b2Reqf140%3d&risl=&pid=ImgRaw&r=0",
            Notes: [
                {
                    NoteName: "C",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/R.4a38845654d2e3487c0be4fc535291d0?rik=jvkK3hdbr4OhVA&riu=http%3a%2f%2fxoax.net%2fchildren%2fref%2fmusic%2fincl%2fscales_octaves%2fmiddle_c_treble_clef.png&ehk=aYg3F0pjbwYRjhTqMWhLM1SIV6kYuTYoBE%2bFwK5vPuM%3d&risl=&pid=ImgRaw&r=0",
                },
                {
                    NoteName: "D",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.WQlmqSeuSnkNchHJrIyIEAAAAA?w=155&h=134&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "E",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.lgUKproo0AbGYQjAyc71iAHaEc?w=264&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "F",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.d_YkVpbFqsZrXB0e_tp8ywAAAA?w=157&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "G",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.EhPQgF81Dm_A-5vs8nsbfAHaEz?w=243&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "A",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.bOM7aad2o7CjQOPJaYsLjAAAAA?w=158&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "B",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.1AbdfTLv1FkESxCH2hKBIwHaGr?w=192&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "C",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.jwotOjW2UItdMzhlMTZ4ogAAAA?w=200&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "D",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.0oKIaW4RldPn1_tREKds5QHaGr?w=176&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "E",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.1QV6r5KzX_y42TLx2p-LOQHaGr?w=179&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "F",
                    Clef: "Treble",
                    Img: "https://th.bing.com/th/id/OIP.2H-SrOenmgtUyKX0P16Y6gHaGr?w=174&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "C",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.108ZW2BZHPaGKlC5xRngPAAAAA?w=189&h=106&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "B",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.ZZT6zOTzk5SdMUjmZ-0q5wAAAA?w=140&h=154&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "A",
                    Clef: "Bass",
                    Img: "https://www.quia.com/files/quia/users/troykay5/musicnotesbass/A_1",
                },
                {
                    NoteName: "G",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.Sfv4XrN_OhyQtC5D7fbfdwHaDt?w=317&h=174&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "F",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.gvBCFlJ5zSFhOnbTczpM1gHaCJ?w=320&h=101&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "E",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.k8VBSX39KIXZFRrxUFAu9gHaFt?w=224&h=179&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "D",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.LjzkuoAXvTo3HNlOX6399gHaDt?w=299&h=174&c=7&r=0&o=5&pid=1.7",
                },
                {
                    NoteName: "C",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.uxPi007mRerlCpJR6KzNxQHaFt?w=202&h=179&c=7&r=0&o=5&pid=1.7",
                },
                 {
                    NoteName: "B",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.iZscitKAYFRLZ9gN5gQ0TQAAAA?w=224&h=179&c=7&r=0&o=5&pid=1.7",
                },
             {
                    NoteName: "A",
                    Clef: "Bass",
                    Img: "https://th.bing.com/th/id/OIP.eoCNFUK2hzVnK42oV-PH0AAAAA?w=209&h=179&c=7&r=0&o=5&pid=1.7",
                },
            ],
        }
    },
    }
</script>


<style>
h1,h2 {
    margin: 0px;
    padding: 0px;
    text-align:center;
}
h1 {
    font-size: 2rem;
}
h2 {
    font-size: 1.5rem;
}
</style>
