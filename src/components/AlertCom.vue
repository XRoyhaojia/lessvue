<template>
    <div class="alert">
        <div class="zhezhao">
            <div class="alertMain">
                <div class="title">
                    温馨提示:{{title}}
                </div>
                <div class="content">
                    {{content}}
                </div>
                <div class="btnList">
                    <div class="btn cancel" @click="cancelE">
                        取消
                    </div>
                    <div class="btn confirm" @click="confirmE">确认</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    

props:['cancelE','confirmE','title','content']
}
</script>

<style lang="less">

@zzopacity:0.3;
@theme-color:orange;
@default-size:18px;
@font-color:#fff;

.fullscreen() {
    width: 100vw;
    height: 100vw;
    display: flex;
}
.defultPadding(){
    padding: 10px
}
.btn() {
    padding: 20px;
    width: 50%;
    text-align: center;
    font-weight: 700;
}
.alert {
   .fullscreen(); 
    .zhezhao {
        .fullscreen();
        background: rgba(0, 0, 0, @zzopacity);
        justify-content: center;
        align-items: center;

        .alertMain{
                position: relative;
                width: 600px;
                height: 400px;
                background: #fff;
                display: flex;
                flex-direction: column;
                .title {
                    font-size: @default-size;
                    height: 50px;
                    background: @theme-color;
                    color: @font-color;
                    .defultPadding();
                    line-height: 50px;
                    font-weight: 700;
                }
                .content {
                    .defultPadding();
                    font-size: @default-size;
                }
                .btnList {
                    position: absolute;
                    display: flex;
                    left: 0;
                    bottom: 0;
                    width: 100%;
                    .cancel {
                        
                        
                        left: 0;

                       .btn();
                        background: chartreuse;
                    }
                    .confirm {
                        
                        
                        right: 0;
                       .btn();
                        background:hotpink
                    }
                }
            }


    }
   
}

</style>