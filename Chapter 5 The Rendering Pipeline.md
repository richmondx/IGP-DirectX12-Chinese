# <element id = "5"> Chapter 5 THE RENDERING PIPELINE </element>

������Ҫ���ܵ�����Ⱦ�ܵ���
����һ��3D������һ�����������Ⱦ�ܵ���������ǽ���������������ݻ��Ƶ�һ��2D��ͼƬ������(ͼƬ[5.1](#Image5.1))��
��һ�µĴ󲿷�����������֪ʶ����һ�����ǽ���ʹ��`Direct3D`����ϰ��λ��ơ�
�����ǿ�ʼ����Ⱦ�ܵ�֮ǰ�����ǻ�������С����������Ҫ�Ƚ������Ȼὲ��һЩ3D����(������ͨ��һ��2D��Ļȥ��һ��3D������)��Ȼ�����ǽ��������ɫ����γ��ֵġ�

**Ŀ��**

-  ������2DͼƬȥ����һ��3D����Ĺؼ���
-  �����������ʹ��`Direct3D`����3D���塣
-  ѧϰ������Ķ��塣
-  ������Ⱦ�ܵ�������3D����������2DͼƬ�Ĺ��̡�

<img src="Images/5.1.png" id = "Image5.1"> </img>

�����ͼƬ�ǴӲ��濴��������м������Ǵ����濴����������ұ����ž���������Ǹ�λ�ÿ��������
���ǿ��Կ�������������������һ��4��׶�����ǳ�֮Ϊ��׶�壬�����ܹ������ķ�Χ������׶��ķ�Χ������׶�巶Χ���������û�а취�����ġ�


## <element id = "5.1"> 5.1 THE 3D ILLUSION </element>

������̤��3D�����ͼ��֮��֮ǰ�����ǻ���һ���򵥵�����û�н����
������ν�һ��3D������ʾ��һ��2D��Ļ��ȥ��
�Һõ��ǣ���������Ѿ��о��ĺ����ˣ�����ͬ���������о��˼���������ν�������õĻ���������һ����
�ڱ����У����ǽ��г�������ͼƬ���ӽ�3D�����Ĺؼ�������

�����㿴��һ��û�������ĺܳ�����·������֪��������·���ߵ�����϶���ƽ�еģ�������վ����·�Ͽ���·�Ļ�����ᷢ����·�������������ԽԶ�Ϳ���Խ���������뵽�����޵�ʱ�����Ǿͻ��ཻ�ˡ�
��������������Ӿ�ϵͳ��һ���ص㣬ƽ������Զ���ῴ���ཻ��һ�����ˡ��μ�ͼƬ[5.2](#Image5.2)��

<img src="Images/5.2.png" id = "Image5.2"> </img>

��һ���ص��������Ĵ�С�����ž����������Եñ�С����ͬһ�����������ǽ��Ŀ��������������Զ�Ĵ�
����һ��������Զ�ķ��ӻῴ������С���������ǽ���һ����ȴ�ῴ�����ܴ�
ͼƬ[5.3](#Image5.3)����ʾ�����尴����������ľ���ڷţ����ԽԶ�����忴����ԽС������ʵ���ǵĴ�Сһ����
ͬ����Ҳ�ᷢ�ֵ���������㹻Զ��ʱ�����Ǿͻῴ���������һ�����ˡ�

<img src="Images/5.3.png" id = "Image5.3"> </img>

����֪��������ص�(�μ�ͼƬ[5.4](#Image5.4))��
��͸����������ס����������������һ���֡�
����һ������Ҫ�ķֱ���������ͨ����������ܹ��õ������Զ����ϵ��������
�����Ѿ��ڵ�4��������`Direct3D`����ʹ����Ȼ���������һ�������Ƿ�ᱻ�ڵ��Լ��Ƿ���Ҫ���ơ�

<img src="Images/5.4.png" id = "Image5.4"> </img>

˼��ͼƬ[5.5](#Image5.5)�������һ��û�й��յ����ұ�����һ�����յ���
����Է�����ߵ���Ƚϱ�ƽ�����������ܲ�����ֻ��һ��Բ��
���Դ����￴�������պ���Ӱ������һ��ʵ���3D�����кܴ����á�

<img src="Images/5.5.png" id = "Image5.5"> </img>

���ͼƬ[5.6](#Image5.6)��ʾ��һ���ɴ�������Ӱ�ӡ�
����Ӱ�Ӹ������ṩ�������ؼ�����Ϣ����һ���������������˹�Դ���ģ��ڶ��������������������������ĸ߶ȡ�

<img src="Images/5.6.png" id = "Image5.6"> </img>

��Ȼ�ⶼ���ճ��кܳ�����������������ܹ�����������ȷ�����������Щ������Ҳ����������ѧϰ��ʹ��3D�����ͼ�ε�ʱ����Щ���������Ժ����治�����������ߺ��ԡ�

## <element id = "5.2"> 5.2 MODEL REPRESENTATION </element>

һ��������3D������Խ��Ƶ�������������ȥ���֡�
��������ξ������ǹ���ģ�͵Ļ����Ĳ��֡�
ͼƬ[5.7](#Image5.7)���ǿ��Կ���һЩ3D����ʹ�����������������ơ�
ͨ����˵�����ʹ�õ�����������Խ�࣬��Ϳ��������ģ�͵�ϸ�ڸ��ӷḻ��
��ͬ����Ҳ�����Ч���ϵĸ���������Ҫ�����������ξͻ�Խ�ࡣ�������֮����Ҫƽ��á�
�������һЩ����£����ǿ�����Ҫ���Ƶ��ǵ���ߣ�����������Ҫ����һ�����ߣ����Ǿͻ�ʹ�ö���߶����ƽ�������ߡ�

<img src="Images/5.7.png" id = "Image5.7"> </img>

���Կ���ͼƬ[5.7](#Image5.7)�е�ģ�����������������ɵġ�
���ںܶ�ģ�͵������������ܶ࣬��˹���һ��ģ�;ͱ�ü����鷳��
Ҳ��˳�����һЩ����ĳ���������ƺ͹���ģ�͡�
��Щ�����ܹ�������ʹ�úܶ๤�߲��ҿ��ӻ�����ƺ͹���ģ�͡�
����[3D Studio Max](https://www.autodesk.com/products/3ds-max/overview), [LightWave 3D](https://www.lightwave3d.com/), [Maya](https://www.autodesk.com/products/maya/overview), [Softimage|XSI](https://www.autodesk.com/products/softimage/overview), [Blender](https://www.blender.org/)(��ѿ�Դ)��

�ڱ����У�����ͨ���ֹ�����ģ�ͻ���ʹ����ѧ��ʽ����һЩ��ģ�ͣ��������壬Բ׶��Բ���ȡ�
�ڱ���ĵ������֣����ǽ�����ʾ��μ���һ��ģ�Ͳ��һ�������

## <element id = "5.3"> 5.3 BASIC COMPUTER COLOR </element>

���������ʾ����ÿһ��������ʵ����ͨ������⣬�̹⣬�����Ϸ������Ӷ���ʾ��������ɫ��
����ϵĹ��䵽�۾��������Ĥ��ʱ������Ĥϸ�����ܵ��̼������񾭳嶯�����ǵĴ��ԣ�Ȼ����Խ�����嶯����ʶ��Ϊ��ɫ��
�����Ļ�ϱ���(**�����ǿ��**)��ͬ����ô�������񾭳嶯Ҳ�᲻ͬ���Ӷ�����Ҳ��ʶ��ɲ�ͬ����ɫ��
ͼƬ[5.8](#Image5.8)�ٳ���һЩ��ͬ�����Ļ�ϻ�õ�ʲô��ɫ�����ӣ��Լ���ͬǿ���µĺ�⡣
������ǾͿ��Ի�ϲ�ͬǿ�ȵĹ����õ����ָ�������ɫ��������Ҫ����ɫ��

����һ����ɫ�кܶ��ַ����������ڳ���������ʵľ���ʹ��`RGB`(**red, green, blue**)������������**Adobe Photoshop**��**Win32**��ѡ����ɫ��

<img src="Images/5.8.png" id = "Image5.8"> </img>

<img src="Images/5.9.png" id = "Image5.9"> </img>

һ����ʾ�������Ĳ�ͬ����ɫ�Ĺ��ǿ��Ҳ�������Ƶġ�
�������ʹ�� **[0.0, 1.0]** �����Χ��ֵ���������ǿ�ȣ�0������û�У�1���������ǿ�ȡ�
���� **(0.25, 0.67, 1.00)** ����ζ�� **25%** �ĺ�⣬ **67%** ���̹�� **100%** �����⡣
��������ʽҲ���������ǿ���ʹ��һ����ά����������һ����ɫ��Ȼ��������ÿһ��ά�ȶ���������һ����ɫ��ǿ�ȡ�

### <element id = "5.3.1"> 5.3.1 Color Operations </element> 

���Ǽ�Ȼʹ�������洢��ɫ����ôҲ�ʹ��������ǿ��Զ���ɫ����һЩ���������㡣�������ǿ��Զ���ɫ���Ӽ���

**<center>(0.0, 0.5, 0) + (0, 0.0, 0.25) = (0.0, 0.5, 0.25)</center>**

**<center>(1, 1, 1) - (1, 1, 0) = (0, 0, 1)</center>**


��ȻҲ���Խ��г˷���

**<center>0.5 x (1, 1, 1) = (0.5, 0.5, 0.5)</center>**

**<center>(r, g ,b) x (x, y ,z) = (rx, ry, rz)</center>**

�����ڽ�������Ĺ����������������ֵ�� **[0, 1]** ֮�⣬�������ǽ����ڳ��ֵ���ʾ����ʱ�򽫱�0С�Ŀ���0����1��Ŀ���1��

### <element id = "5.3.2"> 5.3.2 128-Bit Color </element>

����ͨ���������¼��ɫ����������һ��������������ֵ(`Alpha`)��
����������ͨ�����ڻ��(`Blending`)����������ɫ�Ĳ�͸���ȡ��������ڲ�ʹ�û�ϣ��͵�������Ϊ1�ͺ��ˡ�

�����˰��������������ǵ���ɫ�����ͱ����һ����ά������(r, g, b, a)��
��������һ����ά���������ǿ���ʹ��`XMVECTOR`���Ż�������Ȼ��Ҳ����ʹ�����������Ƶ����Ż�����
`XMVECTOR`ʹ����`SIMD`ָ�����Ż��������㣬��ʵ������һ��128bit��С�����ͱ����������ʹ�������ȥ����[DirectXMath](https://msdn.microsoft.com/en-us/library/windows/desktop/hh437833(v=vs.85))��
�����ʹ�õ���C#�Ļ�����ô��.NET 4.6.2���ϵİ汾�����Ѿ�����֧����`SIMD`ָ���������
