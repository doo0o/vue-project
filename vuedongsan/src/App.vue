    <template>
        <div class="menu">
            <a href="javascript:;"  v-for="gnbFor in gnbArray" :key="gnbFor">{{gnbFor}}</a>
        </div>
        <div>
            <h4>{{products[0]}}</h4>
            <p>50만원</p>
        </div>
        <div>
            <h4>{{products[1]}}</h4>
            <p>50만원</p>
        </div>
        <div>
            <h4>{{products[2]}}</h4>
            <p>50만원</p>
        </div>
    </template>

    <script>

    export default {
    name: 'App',
    data(){
        return{
        gnbArray : ['Home','Shop','About'],
        products : ['역삼동원룸', '의정부원룸', '녹양동원룸'],
        }
    },
    components: {
    }
    }
    </script>

    <style>
    #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
    }
    .menu {
    background : darkslateblue;
    padding : 15px;
    border-radius : 5px;
    }
    .menu a {
    color : white;
    padding : 10px;
    }
    </style>
