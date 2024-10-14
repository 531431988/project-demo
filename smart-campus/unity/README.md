## JS与模型交互


### JS>C#
| 方法名  | 说明  | 类型 | 参数  |
| ------------ | ------------ | ------------ | ------------: |
| OnInitDone() | 通知已初始化完成 |    |    |
| SelectBuilding() | 选择楼宇，会出围绕楼的动画光纤 | string | 建筑名字  | 
| CancelSelect() | 取消楼宇选择  |   |   |
| EnterBuilding() | 进入选择的楼宇，整个场景变虚化，凸显该楼宇  |   |   |
| ExitBuilding() | 退出进入的楼宇，整个场景恢复  |   |   |
| SelectFloor() | 选择进入的楼宇的显示层数  | string  | 楼层名称：1 \| 2 \| 3 \| 4 \| 5  |
| SelectDevice() | 显示进入的楼宇的选择的楼层的相应设备  | string |   |
| ShowBlock() | 将场景的楼宇都实化显示，并取消选择  |   |   |
| ShowStreetState() | 显示街道状况，场景将虚化  |   |   |
| HideStreetState() | 关闭街道状况，场景将实化  |   |   |
| ShowAreaState() | 显示区域状况，场景将虚化  |   |   |
| HideAreaState() | 关闭区域状况，场景将实化  |   |   |
|

<br/>

### C#>JS
| 方法名  | 说明  | 类型 | 参数  |
| ------------ | ------------ | ------------ | ------------: |
| UnityMapInfo() | 场景开始后立即向前端发送场景中的楼宇名称和设备类型<br />deviceNames：设备类型数组<br />buildingNames：可选择的楼宇名称数组 | string | {deviceNames:["smoke","light"], buildingNames:["001","002"]|
| UnityClick() | 当鼠标点击楼宇或设备时向前端发送<br />type：点击的类型（building \| device）<br />content：设备为empty<br /> info：{deviceType：设备类型，deviceState：设备状态（Normal \| Warning \| Error \| Off \| On）<br />pointX：点击位置在屏幕中的横轴比例， pointY：点击位置在屏幕中的纵轴比例} | string | {type:"device", content:"empty", info:{deviceType:"smoke", deviceState:"Normal", pointX:0.5, pointX:0.5}} |
| UnityBuildingInfo() | 当进入楼宇时，向前端发送楼宇的名称及楼宇的楼层名称<br />buildingName：楼层名称，floorIndices：可选择的楼层名称数组 | string | {buildingName:"001", floorIndices:["All", "1", "2", "3"]} |
|












