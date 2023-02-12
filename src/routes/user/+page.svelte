<script>
import UserCount from "../../store/UserCount";

//グローバルでの状態管理
const countUpGlobal = () => {
    UserCount.update( n => n + 1);
};
const countDownGlobal = () => {
    UserCount.update( n => n - 1);
};


    
    //ローカルでの状態管理
    let count = 0;

    const countUp = () => {
        count ++;
    }


    const countDown = () => {
        count --;
    }
</script>

<div>
    <p>ローカルステート</p>
    <button on:click={countUp}>
        +
    </button>
    利用者数： {count}
    <button on:click={countDown}>
        -
    </button><br><br><br>

    <p>グローバルステート</p>
    <button on:click={countUpGlobal}>
        +
    </button>
    利用者数： {$UserCount}
    <button on:click={countDownGlobal}>
        -
    </button>
</div>

<style>
    /* your styles go here */
</style>

<!-- markup (zero or more items) goes here -->