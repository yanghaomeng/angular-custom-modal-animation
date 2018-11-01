# ionic modal弹出方式单一，自定义弹入消失动画

## 自定义enterAnimation和leaveAnimation,其他弹窗同理

### 在page中引入
<pre><code>
	import { ModalAlertEnter, ModalAlertLeave } from 'modal-transitions';
	.........


	async changeCompanyNature() {
    	  const myModal = await this.modalCtrl.create({
              component: MyConfirmModalPage,
              enterAnimation: ModalAlertEnter,
              leaveAnimation: ModalAlertLeave
          });
    	  myModal.onDidDismiss().then((returnValue) => {
      	      if (returnValue.data) {
                  console.log(returnValue);
              }
          });
    	  myModal.present();
  	 }
	}
</code></pre>

modal-transition.ts为仿ionic原生alert的动画
