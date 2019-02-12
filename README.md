# RenderPal v2 Update

**Submitter conf**

```Job settings -> Net job -> Scene -> (Need to select scene)```

```Render settings -> Files and directories -> Project dir -> (Need to select project dir)```

```Render settings -> Additional render settingss -> General -> (can enable command line arguments)```

**Renderer management**

*To add command line arguments:*
- Open Parametrs tab
- Press the button 'Add parametrs' (can also choose already built in parameters)
- write ID, select Group, write diplay name and help text
- Select Type: Switch and Press OK
- Then Select created parametr and press the button 'Create Switch' 
- write command line argument in Switch field and press OK
 







# Unity-CMD

**To start Unity project from CMD:**

``` start <Path to Unity.exe> -projectPath <Path to project> ```

  example
  
```start C:\"Program Files"\2018.2.15f1\Editor\Unity.exe -projectPath D:\Documents\Work\RenderFarmTest```



**To execute static method for Unity project from CMD:**

```start <Path to Unity.exe> -projectPath <Path to project> -executeMethod <namespace.class.method>```

  example
  
```start C:\"Program Files"\2018.2.15f1\Editor\Unity.exe -projectPath D:\Documents\Work\RenderFarmTest -executeMethod myNameSpace.myClass.myMethod```

**Static script example:**

Script location in procejt -> Assets/Editor

```
using UnityEngine;
using UnityEditor;
using System;

namespace myNameSpace
{
   class myClass
   {
       public static void myMethod()
       {
          string[] parameters;   
          parameters = Environment.GetCommandLineArgs();  // hold all cmd parameters
          // Do everything needed to handle rendersetings bla bla bla
          UnityEditor.EditorApplication.isPlaying = true;
       
       }
   }
}
```
[Unity doc](https://docs.unity3d.com/Manual/CommandLineArguments.html)

[Blog post with example](http://www.kinematicsoup.com/news/using-the-command-line-toolset-to-run-unity-tests)
