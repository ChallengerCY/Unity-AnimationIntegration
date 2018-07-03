# Unity-AnimationIntegration
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Animation允许两个状态之间通过Unity animation system使用完整的animation进行过度,这是最强大的过渡模式，支持多属性可以同时进行动画。

![AnimationIntegration](https://github.com/ChallengerCY/Unity-AnimationIntegration/blob/master/TestAnimationIntegration/Picture%26Gif/Animation%20Integration.gif)

>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;使用Animation transition Mode，需要在控制元素上面添加一个Animator组件。可以通过点击Auto Generate Animation去自动生成。在这个过程中生成了一个已经保存了需要过度的状态的Animator Controller。

![GUI_ButtonInspectorAnimation](https://github.com/ChallengerCY/Unity-AnimationIntegration/blob/master/TestAnimationIntegration/Picture%26Gif/GUI_ButtonInspectorAnimation.png)

>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;新的Animator controller可以直接使用。不像大多数Animator Controllers，这个控制器还存储用于控制器过度的动画，如果需要的话，这些动画可以定制。

![GUI_ButtonAnimator](https://github.com/ChallengerCY/Unity-AnimationIntegration/blob/master/TestAnimationIntegration/Picture%26Gif/GUI_ButtonAnimator.png)

>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
例如，如果选择一个带有Animator controller 的按钮元素，可以通过打开Animation window (Window>Animation)来编辑按钮的每个状态的动画。通过 Animation Clip pop-up菜单去选择需要剪辑的动画。可以选择 “Normal”, “Highlighted”, “Pressed” and “Disabled”。

![GUI_ButtonAnimationWindow](https://github.com/ChallengerCY/Unity-AnimationIntegration/blob/master/TestAnimationIntegration/Picture%26Gif/GUI_ButtonAnimationWindow.png)

>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Normal状态就是Button没有任何操作下的状态，可以为空。其他所有的状态，最常见的配置是在时间线开始时的单个关键帧。两个状态之间的过渡由Animator来控制。
举个例子，通过Animation Clip pop up菜单选中Highlighted state，并在timeline的开始设置button的宽度，就可以在button是Highlighted状态时播放一个过渡动画。具体步骤是 选择对应的Butotn，通过inspector改变Button的宽度，退出编辑。在一帧当中可以设置很多参数的变化。多个Button也可以公用同一个Animator Controllers。

>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;UI Animation transition mode和Unity legacy animation system并不兼容，应该只使用Animator Component。