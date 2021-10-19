# Android_OS_Check
Android OS 업데이트 내역 및 체크사항

## Android 11 대응 내역(개인정보 보호 강화)
1. 범위 저장소 액세스 변경(Scoped Storage)
2. 패키지 공개 상태 변경
   > AndroidManifest.xml에 선언
   ```
   //패키지 명을 아는 경우
   <manifest package="com.example.game">
      <queries>
          <package android:name="com.example.store" />
          <package android:name="com.example.services" />
      </queries>
     </manifest>

     //이미지 공유 와 같이 상호작용 하는 앱이 특정앱이 아닌 경우 
      <queries>
          <intent>
              <action android:name="android.intent.action.SEND" />
              <data android:mimeType="image/jpeg" />
          </intent>
      </queries>
   </manifest>
   ```
3. 
