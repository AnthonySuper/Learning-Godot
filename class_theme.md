#  Theme  
####**Inherits:** [Resource](class_resource)
####**Category:** Core

###  Brief Description  
Theme for controls.

###  Member Functions 
  * void  **[set&#95;icon](#set_icon)**  **(** [String](class_string) name, [String](class_string) type, [Texture](class_texture) texture  **)**
  * [Texture](class_texture)  **[get&#95;icon](#get_icon)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * [bool](class_bool)  **[has&#95;icon](#has_icon)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * void  **[clear&#95;icon](#clear_icon)**  **(** [String](class_string) name, [String](class_string) type  **)**
  * [StringArray](class_stringarray)  **[get&#95;icon&#95;list](#get_icon_list)**  **(** [String](class_string) arg0  **)** const
  * void  **[set&#95;stylebox](#set_stylebox)**  **(** [String](class_string) name, [String](class_string) type, [StyleBox](class_stylebox) texture  **)**
  * [StyleBox](class_stylebox)  **[get&#95;stylebox](#get_stylebox)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * [bool](class_bool)  **[has&#95;stylebox](#has_stylebox)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * void  **[clear&#95;stylebox](#clear_stylebox)**  **(** [String](class_string) name, [String](class_string) type  **)**
  * [StringArray](class_stringarray)  **[get&#95;stylebox&#95;list](#get_stylebox_list)**  **(** [String](class_string) arg0  **)** const
  * void  **[set&#95;font](#set_font)**  **(** [String](class_string) name, [String](class_string) type, [Font](class_font) font  **)**
  * [Font](class_font)  **[get&#95;font](#get_font)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * [bool](class_bool)  **[has&#95;font](#has_font)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * void  **[clear&#95;font](#clear_font)**  **(** [String](class_string) name, [String](class_string) type  **)**
  * [StringArray](class_stringarray)  **[get&#95;font&#95;list](#get_font_list)**  **(** [String](class_string) arg0  **)** const
  * void  **[set&#95;color](#set_color)**  **(** [String](class_string) name, [String](class_string) type, [Color](class_color) color  **)**
  * [Color](class_color)  **[get&#95;color](#get_color)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * [bool](class_bool)  **[has&#95;color](#has_color)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * void  **[clear&#95;color](#clear_color)**  **(** [String](class_string) name, [String](class_string) type  **)**
  * [StringArray](class_stringarray)  **[get&#95;color&#95;list](#get_color_list)**  **(** [String](class_string) arg0  **)** const
  * void  **[set&#95;constant](#set_constant)**  **(** [String](class_string) name, [String](class_string) type, [int](class_int) constant  **)**
  * [int](class_int)  **[get&#95;constant](#get_constant)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * [bool](class_bool)  **[has&#95;constant](#has_constant)**  **(** [String](class_string) name, [String](class_string) type  **)** const
  * void  **[clear&#95;constant](#clear_constant)**  **(** [String](class_string) name, [String](class_string) type  **)**
  * [StringArray](class_stringarray)  **[get&#95;constant&#95;list](#get_constant_list)**  **(** [String](class_string) arg0  **)** const
  * void  **[set&#95;default&#95;font](#set_default_font)**  **(** [Object](class_object) font  **)**
  * [Object](class_object)  **[get&#95;default&#95;font](#get_default_font)**  **(** **)** const
  * [StringArray](class_stringarray)  **[get&#95;type&#95;list](#get_type_list)**  **(** [String](class_string) arg0  **)** const
  * void  **[copy&#95;default&#95;theme](#copy_default_theme)**  **(** **)**

###  Description  
Theme for skinning controls. Controls can be skinned individually, but for complex applications it's more efficient to just create a global theme that defines everything. This theme can be applied to any [Control](class_control), and it and the children will automatically use it.

	Theme resources can be alternatively loaded by writing them in a .theme file, see wiki for more info.

###  Member Function Description  
