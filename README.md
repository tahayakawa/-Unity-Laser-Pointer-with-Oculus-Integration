# -Unity-Laser-Pointer-with-Oculus-Integration


UnityのVRでコントローラーや目線からレーザーポインターを出す方法

VRのUI操作でよく使われる

## 実行環境

Unity 2020.3.27f1

Oculus Integration version 35.0

## レーザー出す

1. Oculus Integration ダウンロード
2. Assets\Oculus\VR\Prefabs からOVRCameraRigをヒエラルキーに出す（UnityデフォルトのXRRigは使わない）
3. Create Empty でOVRLaserPointerを作る
4. その子オブジェクトに3D Object > Quad を作成。 Collider は削除

![image](https://user-images.githubusercontent.com/102804813/186377485-c7f3c374-96ef-44b5-8ccd-443df9eeb16b.png)

5. OVRLaserPointerにOVR Laser Pointer スクリプトを貼り付け

![image](https://user-images.githubusercontent.com/102804813/186377602-6256371c-101f-4393-aae7-9ff75cf6e6fe.png)

