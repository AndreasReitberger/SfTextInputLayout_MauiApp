# SfTextInputLayout_MauiApp
Repro for a syncfusion issue.

![image](https://github.com/AndreasReitberger/SfTextInputLayout_MauiApp/assets/2952443/234af790-a0a9-4230-b950-e0ccbdcf16f3)

```xaml
<Entry
    Text="{Binding Name, Mode=TwoWay}" 
    Keyboard="Default"
    />

<!-- Entry -->
<core:SfTextInputLayout
     Style="{StaticResource Style.Syncfusion.SfTextInputLayout.Default}"
     Hint="Name"
     ErrorText=""
     ContainerBackground="Green"
     >
    <Entry
         Background="{Binding Source={RelativeSource AncestorType={x:Type core:SfTextInputLayout}}, Path=Background}"
         Text="{Binding Name, Mode=TwoWay}" 
         Keyboard="Default"
         />
</core:SfTextInputLayout>

<!-- Numeric -->
<core:SfTextInputLayout
     Style="{StaticResource Style.Syncfusion.SfTextInputLayout.Default}"
     Hint="Numeric"
     ErrorText=""
     ContainerBackground="AliceBlue"
     >
    <inputs:SfNumericEntry
          Background="{Binding Source={RelativeSource AncestorType={x:Type core:SfTextInputLayout}}, Path=Background}"
          Value="{Binding Quantity, Mode=TwoWay}" 
          Margin="5,0"
          />
</core:SfTextInputLayout>

<!-- Numeric -->
<core:SfTextInputLayout
     Style="{StaticResource Style.Syncfusion.SfTextInputLayout.Default}"
     Hint="Numeric"
     ErrorText=""
     >
    <inputs:SfNumericEntry
          Style="{StaticResource Style.Syncfusion.SfNumericEntry.Default}"
          Background="Transparent"
          Value="{Binding Quantity, Mode=TwoWay}" 
          Margin="5,0"
          />
</core:SfTextInputLayout>
```
