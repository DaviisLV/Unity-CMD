# Unity-CMD

**To start Unity project from CMD:**

``` start <Path to Unity.exe> -projectPath <Path to project> ```

  example
  
```start C:\"Program Files"\2018.2.15f1\Editor\Unity.exe -projectPath D:\Documents\Work\RenderFarmTest```



**To execute static method for Unity project from CMD:**

```start <Path to Unity.exe> -projectPath <Path to project> -executeMethod <namespace.class.method>```

  example
  
```start C:\"Program Files"\2018.2.15f1\Editor\Unity.exe -batchmode -projectPath D:\Documents\Work\RenderFarmTest -executeMethod myNameSpace.myClass.myMethod```

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
