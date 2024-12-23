```mermaid

erDiagram
    User {
        int userId PK "用戶ID"
        string name "姓名"
        date birthDate "生日"
        string gender "性別"
    }
    HistoryRecord {
        int recordId PK "歷史記錄ID"
        int userId FK "用戶ID"
        float strideLength "步幅長度(米/步)"
        float walkingSpeed "行走速度(米/秒)"
        float averageStepLength "每步行步長度(米)"
        float leftFootAngle "左腳Y軸角度值"
        float rightFootAngle "右腳Y軸角度值"
        date measurementTime "採集時間"
        string deviceName "設備名稱"
        string deviceType "設備類型"
    }

    User ||--o{ HistoryRecord : "擁有"
![image](https://github.com/user-attachments/assets/8e367399-5023-4ce1-b515-1af8470e6471)

```
