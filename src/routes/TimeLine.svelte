

<div class="timeline">
    <div class="wrapper left">
        <div class="content">
            <h3>India</h3>
            <p>name</p>
        </div>
    </div>
    <div class="wrapper right">
        <div class="content">
            <h3>japan</h3>
            <p>name</p>
        </div>
    </div>
</div>

<style>
    .timeline{
        position: relative;
        max-width: 40vw;
        margin: 0 auto;
    }
    .timeline::after{
        content: '';
        position: absolute;
        width: 6px;
        top:0;
        bottom: 0;
        left: 50%;
        margin-left: -3px;
    }

    .wrapper{
    padding: 10px 40px;
    position: relative;
    background-color: #474e5d;
    width: 50%;
    }

    .wrapper::after{
    content: '';
    position: absolute;
    width: 25px;
    height: 25px;
    right: -17px;
    border: 4px solid #FF9F55;
    top: 15px;
    border-radius: 50%;
    z-index: 1;
    }

    .left{
        left: 0;
    }
    .right{
        left: 50%;
    }

    .left::before{
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    right: 30px;
    border: medium solid white;
    border-width: 10px 0 10px 10px;
    border-color: transparent transparent transparent white;
    }
    
    .right::after {
     left: -16px;
      }
    
 .content {
  padding: 20px 30px;
  background-color: white;
  position: relative;
  border-radius: 6px;
}
</style>