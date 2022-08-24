# -Unity- Laser Pointer with Oculus Integration


UnityのVRでコントローラーや目線からレーザーポインターを出す方法

VRのUI操作でよく使われる

## 実行環境

Unity 2020.3.27f1

Oculus Integration version 35.0

## レーザー出す

1. Oculus Integration ダウンロード。UnityのProjectSettingsでOculusにチェック
2. Assets\Oculus\VR\Prefabs からOVRCameraRigをヒエラルキーに出す（UnityデフォルトのXRRigは使わない）
3. Create Empty でOVRLaserPointerを作る
4. その子オブジェクトに3D Object > Quad を作成。 Collider は削除

![image](https://user-images.githubusercontent.com/102804813/186377485-c7f3c374-96ef-44b5-8ccd-443df9eeb16b.png)

5. OVRLaserPointerにOVR Laser Pointer スクリプトをつける。マテリアルLaserをつける

![image](https://user-images.githubusercontent.com/102804813/186377602-6256371c-101f-4393-aae7-9ff75cf6e6fe.png)

6. PointerIconに OVR Overlay をつける
7. プロジェクトビューで"gaze"と検索し、PointerIconのマテリアルにGazePointer、TexturesにGazeRingをつける

OVR Overlayの設定も同じにする

![image](https://user-images.githubusercontent.com/102804813/186381353-b376ba92-67a9-44a5-be23-08c705f3efaf.png)

8. 右手ならRightControllerAnchorの子にCreateEmptyする。目線ならCenterEyeAnchor

![image](https://user-images.githubusercontent.com/102804813/186383688-7b3bad49-0fa2-4904-904d-f8441065a757.png)

9. OVR Laser Pointer のインスペクターをいい感じにする。Line RendererのWidthでレーザーの幅を調整

![image](https://user-images.githubusercontent.com/102804813/186384451-2007749e-69ba-40e3-9bbb-f0f2714fde53.png)

10. UI>EventSystemを作成。Standalone Input Moduleのチェックを外す。
11. OVR Input Moduleをつける。インスペクターもいい感じにする

![image](https://user-images.githubusercontent.com/102804813/186386199-76230b69-3940-4471-9896-12d1569c5b34.png)

12. Canvasを作成。インスペクターを画像の通りにする。

![image](https://user-images.githubusercontent.com/102804813/186388970-e7574150-58e8-401b-a338-23d7497b97a7.png)

13. Canvas内にボタンやパネルを入れれば完成

