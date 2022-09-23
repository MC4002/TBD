<template>
<div>
    <h1>Music Note Sightreading</h1>
    <h2>Treble and Bass Clef Only</h2>
    <h2>Alto and Tenor Clef are unavailable.</h2>
    <h2>20 Notes in Total: 2 Octaves Lower A to 2 Octaves Upper F</h2>
    <h2>(In Comparsion to Middle C)</h2>
    <button v-on:click="NotesDisplay">Click to get a new Note</button>
    <h2></h2>
    <img class="NoteIMG" :src="Picture" alt="Whole Note"/>
    <h2>Hover below to check the note name.</h2>
    <h2 class="NoteName"> The Note Name is {{ NoteName }}.</h2>
</div>
</template>

<script>

export default {
    name: "TBD",
    components: {},
    data () {
        return {
            Picture: "",
            NoteName: "",
            Notes: [
                {
                    Name: "C",
                    Img: "https://th.bing.com/th/id/R.4a38845654d2e3487c0be4fc535291d0?rik=jvkK3hdbr4OhVA&riu=http%3a%2f%2fxoax.net%2fchildren%2fref%2fmusic%2fincl%2fscales_octaves%2fmiddle_c_treble_clef.png&ehk=aYg3F0pjbwYRjhTqMWhLM1SIV6kYuTYoBE%2bFwK5vPuM%3d&risl=&pid=ImgRaw&r=0",
                },
                {
                    Name: "D",
                    Img: "https://th.bing.com/th/id/OIP.WQlmqSeuSnkNchHJrIyIEAAAAA?w=155&h=134&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "E",
                    Img: "https://th.bing.com/th/id/OIP.lgUKproo0AbGYQjAyc71iAHaEc?w=264&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "F",
                    Img: "https://th.bing.com/th/id/OIP.d_YkVpbFqsZrXB0e_tp8ywAAAA?w=157&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "G",
                    Img: "https://th.bing.com/th/id/OIP.EhPQgF81Dm_A-5vs8nsbfAHaEz?w=243&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "A",
                    Img: "https://th.bing.com/th/id/OIP.bOM7aad2o7CjQOPJaYsLjAAAAA?w=158&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "B",
                    Img: "https://th.bing.com/th/id/OIP.1AbdfTLv1FkESxCH2hKBIwHaGr?w=192&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "C",
                    Img: "https://th.bing.com/th/id/OIP.jwotOjW2UItdMzhlMTZ4ogAAAA?w=200&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "D",
                    Img: "https://th.bing.com/th/id/OIP.0oKIaW4RldPn1_tREKds5QHaGr?w=176&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "E",
                    Img: "https://th.bing.com/th/id/OIP.1QV6r5KzX_y42TLx2p-LOQHaGr?w=179&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "F",
                    Img: "https://th.bing.com/th/id/OIP.2H-SrOenmgtUyKX0P16Y6gHaGr?w=174&h=180&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "C",
                    Img: "https://th.bing.com/th/id/OIP.108ZW2BZHPaGKlC5xRngPAAAAA?w=189&h=106&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "B",
                    Img: "https://th.bing.com/th/id/OIP.ZZT6zOTzk5SdMUjmZ-0q5wAAAA?w=140&h=154&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "A",
                    Img: "https://www.quia.com/files/quia/users/troykay5/musicnotesbass/A_1",
                },
                {
                    Name: "G",
                    Img: "https://th.bing.com/th/id/OIP.Sfv4XrN_OhyQtC5D7fbfdwHaDt?w=317&h=174&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "F",
                    Img: "https://th.bing.com/th/id/OIP.gvBCFlJ5zSFhOnbTczpM1gHaCJ?w=320&h=101&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "E",
                    Img: "https://th.bing.com/th/id/OIP.k8VBSX39KIXZFRrxUFAu9gHaFt?w=224&h=179&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "D",
                    Img: "https://th.bing.com/th/id/OIP.LjzkuoAXvTo3HNlOX6399gHaDt?w=299&h=174&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "C",
                    Img: "https://th.bing.com/th/id/OIP.uxPi007mRerlCpJR6KzNxQHaFt?w=202&h=179&c=7&r=0&o=5&pid=1.7",
                },
                 {
                    Name: "B",
                    Img: "https://th.bing.com/th/id/OIP.iZscitKAYFRLZ9gN5gQ0TQAAAA?w=224&h=179&c=7&r=0&o=5&pid=1.7",
                },
                {
                    Name: "A",
                    Img: "https://th.bing.com/th/id/OIP.eoCNFUK2hzVnK42oV-PH0AAAAA?w=209&h=179&c=7&r=0&o=5&pid=1.7",
                },
            ],
        }
    },
    methods: {
        NotesDisplay () {
            var Display = Math.floor(Math.random()*this.Notes.length);
            var PIC = this.Notes[Display].Img;
            var NN = this.Notes[Display].Name;
            this.Picture = PIC;
            this.NoteName = NN;
        },
    },
    }
</script>


<style>
html,
body,
* {
  margin: 0%;
  padding: 0%;
  color: black;
  text-align: center;
  align-content: center;
}
h1 {
    font-size: 2rem;
}
h2 {
    font-size: 1.5rem;
}
.NoteIMG {
    height: 55%;
    margin-top: 5px;
}
.NoteName {
    color: white;
    margin-top: 5px;
    border: 2px solid darkslateblue;
}
.NoteName:hover {
    color: black;
}
</style>
