- [ジョーンズベクトル](#ジョーンズベクトル)
  - [直線偏光](#直線偏光)
  - [円偏光](#円偏光)
- [ジョーンズ行列](#ジョーンズ行列)
  - [1/2波長板](#12波長板)
  - [1/4波長板](#14波長板)
  - [SLM](#slm)
- [偏光子とポアンカレ球](#偏光子とポアンカレ球)
  - [射影演算子](#射影演算子)
  - [パウリ行列展開](#パウリ行列展開)
  - [ポアンカレ球](#ポアンカレ球)
  - [高次元ポアンカレ球](#高次元ポアンカレ球)
- [ブロッホ球](#ブロッホ球)
  - [高次元ブロッホ球](#高次元ブロッホ球)
- [論文解説](#論文解説)
  - [SLM2個使ってベクトルビームを作る](#slm2個使ってベクトルビームを作る)
    - ["Polarization distribution control of parallel femtosecond pulses with spatial light modulators"](#polarization-distribution-control-of-parallel-femtosecond-pulses-with-spatial-light-modulators)
    - ["Holographic femtosecond laser manipulation for advanced material processing"](#holographic-femtosecond-laser-manipulation-for-advanced-material-processing)
    - ["Flexible generation of the generalized vector vortex beams"(2021)](#flexible-generation-of-the-generalized-vector-vortex-beams2021)
  - [ベクトルビームと機械学習](#ベクトルビームと機械学習)
    - ["Machine learning-based classification of vector vortex beams"](#machine-learning-based-classification-of-vector-vortex-beams)
  - [ベクトルビームと幾何学](#ベクトルビームと幾何学)
    - ["Observation of optical polarization Möbius strips"](#observation-of-optical-polarization-möbius-strips)
    - ["Full Poincare´ beams"](#full-poincare-beams)
    - ["Generation of A Space-Variant Vector Beam with Catenary-Shaped Polarization States"](#generation-of-a-space-variant-vector-beam-with-catenary-shaped-polarization-states)
  - [Gouy位相](#gouy位相)
    - [パンチャラトナムベリー位相](#パンチャラトナムベリー位相)
    - ["光学におけるベリー位相"](#光学におけるベリー位相)
    - ["Manifestation of the Gouy phase in strongly focused, radially polarized beams"](#manifestation-of-the-gouy-phase-in-strongly-focused-radially-polarized-beams)
  - [高次元ポアンカレ球](#高次元ポアンカレ球-1)
    - ["Higher-Order Poincaré Sphere, Stokes Parameters, and the Angular Momentum of Light"](#higher-order-poincaré-sphere-stokes-parameters-and-the-angular-momentum-of-light)
    - ["Generalized Poincare sphere"](#generalized-poincare-sphere)
  - [ベクトルビームの評価方法](#ベクトルビームの評価方法)
    - ["Measuring the nonseparability of vector vortex beams"](#measuring-the-nonseparability-of-vector-vortex-beams)
    - ["Beam quality measure for vector beams"](#beam-quality-measure-for-vector-beams)
    - ["ENTANGLEMENT OF FORMATION AND CONCURRENCE"](#entanglement-of-formation-and-concurrence)
  - [近軸近似のもとでスカラー場に対するヘルムホルツ方程式を解く](#近軸近似のもとでスカラー場に対するヘルムホルツ方程式を解く)
    - ["From Maxwell to paraxial wave optics"](#from-maxwell-to-paraxial-wave-optics)
    - ["Gaussian Beam 計算メモ"](#gaussian-beam-計算メモ)
    - [HGbeam](#hgbeam)
    - [LGbeam](#lgbeam)
    - [ヘルムホルツ方程式の導出](#ヘルムホルツ方程式の導出)
  - [近軸近似のもとでベクトル場に対するヘルムホルツ方程式を解く](#近軸近似のもとでベクトル場に対するヘルムホルツ方程式を解く)
    - [参考:"Separability and Applications"](#参考separability-and-applications)
    - ["Vector-beam solutions of Maxwell's wave equation"](#vector-beam-solutions-of-maxwells-wave-equation)
    - ["Vector Helmholtz–Gauss and vector Laplace–Gauss beams"](#vector-helmholtzgauss-and-vector-laplacegauss-beams)
    - [エルミート多項式](#エルミート多項式)
    - [ラプラシアンを考える](#ラプラシアンを考える)
  - [近軸近似せずにスカラー場のヘルムホルツ方程式を解く](#近軸近似せずにスカラー場のヘルムホルツ方程式を解く)
    - ["Nonparaxial Propagation Properties of Specially Correlated Radially Polarized Beams in Free Space"](#nonparaxial-propagation-properties-of-specially-correlated-radially-polarized-beams-in-free-space)
    - ["Closed-form bases for the description of monochromatic, strongly focused, electromagnetic fields"](#closed-form-bases-for-the-description-of-monochromatic-strongly-focused-electromagnetic-fields)
    - ["Measuring the nonseparability of vector vortex beams"](#measuring-the-nonseparability-of-vector-vortex-beams-1)
- [実験案](#実験案)
  - [その１](#その１)
  - [その２](#その２)
  - [その３](#その３)
- [教科書的な立ち位置](#教科書的な立ち位置)
  - [ベクトルビーム](#ベクトルビーム)
    - ["Cylindrical vector beams: from mathematical concepts to applications"](#cylindrical-vector-beams-from-mathematical-concepts-to-applications)
    - ["Vector Beams for Fundamental Physics and Applications"](#vector-beams-for-fundamental-physics-and-applications)
  - [光渦](#光渦)
    - ["Orbital angular momentum: origins, behavior and applications"](#orbital-angular-momentum-origins-behavior-and-applications)
  - [SLM](#slm-1)
    - ["Creation and detection of optical modes with spatial light modulators"](#creation-and-detection-of-optical-modes-with-spatial-light-modulators)

# ジョーンズベクトル

1941年にアメリカの物理学者ジョーンズ(R. Clark Jones)によって考案された**ジョーンズベクトル**は偏光状態を複素ベクトルによって表すことができる。同じく偏光状態をベクトルで表すストークスベクトルと違いジョーンズベクトルでは完全偏光(直線偏光や楕円偏光など電場の振動方向が規則性を持っているもの。自然光は電場の振動方向がバラバラであり部分偏光と呼ばれている。)の光のみしか扱うことができないがストークスベクトルは4成分なのに対してジョーンズベクトルは2成分となる。偏光素子(偏光状態を別の偏光状態へと偏光させる役割をもつもの)を表現する行列も4行4列から2行2列と小さくなる。
ジョーンズベクトルは以下のように複素ベクトルで表される。

$$
\boldsymbol{E} = 
\begin{bmatrix}
E_{x0} e^{i\varphi_x} \\
E_{y0} e^{i\varphi_y}
\end{bmatrix}
$$

それぞれの振幅や位相の違いによって色々な偏光状態が表される。
例えば振幅が等しく、1に規格化されている時、つまり

$$
\begin{aligned}
E_{x0}^2 + E_{y0}^2 &= 1 \\
2 E_{x0}^2 &= 1 \\
\therefore E_{x0} &= \frac{1}{\sqrt{2}}
\end{aligned}
$$

となり、ジョーンズベクトルは

$$
\begin{aligned}
\boldsymbol{E} &= \frac{1}{\sqrt{2}}
\begin{bmatrix}
e^{i \varphi_x} \\
e^{i \varphi_y}
\end{bmatrix} \\
&= \frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
e^{i(\varphi_y - \varphi_x)}
\end{bmatrix} \\
&= \frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
e^{i\delta}
\end{bmatrix}
\end{aligned}
$$

となる。**以下ではこのように振幅が等しく、規格化されているとする。**

## 直線偏光
例えば位相が共に等しいとき

$$
\boldsymbol{E} = \frac{1}{\sqrt{2}} e^{i \varphi_x}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

となり、これは反時計回りに $\frac{\pi}{4}$ だけ傾いた直線偏光を表している。
***確かにベクトルの成分だけで見ると $\frac{\pi}{4}$ だけ傾いたベクトルだからそう思えるかもしれないが複素数が係数としてかかっているからなんか腑に落ちない***と思う。
そこで実部を取ってみると

$$
Re(\boldsymbol{E}) = \frac{1}{\sqrt{2}} \cos{\varphi_x}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

となり、晴れて実平面で $\frac{\pi}{4}$ だけ傾いた直線偏光が表された。
そもそも波を複素数で表現するのは実部だけ( $\cos$ だけ)で考えると計算が面倒になるという問題を解決するためだったので最終的には実部を取るというのは理にかなっている。
<br>

## 円偏光

次に $x$ 成分が $y$ 成分より $\frac{\pi}{2}$ だけ進んでいる場合を考える。(例えば $x$ 成分が $\cos{\varphi_x}$ なら $y$ 成分は $\cos{(\varphi_x-\frac{\pi}{2})}=\sin{\varphi_x}$ のように波が $y$ 成分の方が $z$ 軸性の方向にずれている)

$$
\begin{aligned}
\varphi_y &= \varphi_x - \frac{\pi}{2} \\
\varphi_y - \varphi_x &= -\frac{\pi}{2}\\
\therefore \delta &= -\frac{\pi}{2}
\end{aligned}
$$

を(1)に代入すると

$$
\begin{aligned}
\boldsymbol{E} &= \frac{1}{\sqrt{2}}
\begin{bmatrix}
e^{i \varphi_x} \\
e^{i (\varphi_x - \frac{\pi}{2})}
\end{bmatrix} \\
&= \frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
e^{-i\frac{\pi}{2}}
\end{bmatrix} \\
&= \frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
-i
\end{bmatrix} \\
\end{aligned}
$$

これは**左回り円偏光**を表している。
これも実部をとると

$$
Re(\boldsymbol{E}) = \frac{1}{\sqrt{2}}
\begin{bmatrix}
\cos{\varphi_x} \\
\sin{\varphi_x}
\end{bmatrix}
$$

<br>

となるがこれは $\varphi_x$ を変化させていくと $x-y$ 平面で左回りに回転するベクトル場になる。

【補足】
上ではこのジョーンズベクトルは左回り円偏光を表しているといったが、右回り円偏光を表していると書いてあるものもあるこれは***座標系をどこから見るかによって起こる問題である。***
座標は右手系が基本なのでz軸が紙面裏面から紙面表面に向かうようにとると垂直方向はx軸に、水平方向はy軸になる。つまり、$z$ 軸正の方向から見るのか、負の方向から見るのかで回り方が逆転する。

～ここに座標系と目の絵を描いて～

***なんでx,yが反転するような立場から考えるの？***
と思うかもしれないがこれは工学系と理学系で光のとらえ方が異なるかららしい。つまり**工学寄りの光学**の分野ではあくまで**主役は光であり**光を迎える視点で考えたいのだと思う。逆に**理学寄りの光学**では**主役は光によって照らされるサンプル**であるので光を送り出す立場で現象を考える。
<br>

同様に $y$ 成分が $x$ 成分より $\frac{\pi}{2}$ だけ遅れている場合を考えると

$$
\boldsymbol{E} = \frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
i
\end{bmatrix}
$$

これは右回り円偏光を表している。
これも実部をとると

$$
Re(\boldsymbol{E}) = \frac{1}{\sqrt{2}}
\begin{bmatrix}
\cos{\varphi_x} \\
-\sin{\varphi_x}
\end{bmatrix}
$$

となり、先ほどとは逆に左回り円偏光になる。
右回り円偏光と左回り円偏光をプロットしてみる。
 $\varphi_x$ を $0$ から $2\pi$ に変化させたときの実ベクトルが指す点の軌跡をベクトル場として描画している。

```python
import numpy as np
import matplotlib.pyplot as plt

pi = np.pi
cos = np.cos
sin = np.sin
phi = pi * np.linspace(0, 2, 32)
length = len(phi)

x = cos(phi)
add_x = np.append(x, 1)
y = sin(phi)
add_y = np.append(y, 0)

u = np.empty(length)
v = np.empty(length)

for i in range(1, length+1):
  u[i-1] = add_x[i] - add_x[i-1]
  v[i-1] = add_y[i] - add_y[i-1]

plt.figure()
plt.axes().set_aspect('equal')
plt.quiver(x, y, u, v, scale=3, color='blue', width=0.007)
plt.xlabel('x axis')
plt.ylabel('y axis')
plt.title('right-handed circular polarization')
plt.grid(True)
plt.show()
```

```python
import numpy as np
import matplotlib.pyplot as plt

pi = np.pi
cos = np.cos
sin = np.sin
phi = pi * np.linspace(0, 2, 32)
length = len(phi)

x = cos(phi)
add_x = np.append(x, 1)
y = -sin(phi)
add_y = np.append(y, 0)

u = np.empty(length)
v = np.empty(length)

for i in range(1, length+1):
  u[i-1] = add_x[i] - add_x[i-1]
  v[i-1] = add_y[i] - add_y[i-1]

plt.figure()
plt.axes().set_aspect('equal')
plt.quiver(x, y, u, v, scale=3, color='blue', width=0.007)
plt.xlabel('x axis')
plt.ylabel('y axis')
plt.title('left-handed circular polarization')
plt.grid(True)
plt.show()
```

繰り返すが光学ではレーザーは$x-y$平面を裏側から(紙面裏側から紙面表側)から見ることに注意。

ここで左右円偏光を表す2つのベクトルの内積をとってみると

$$
\frac{e^{2i\varphi_x}}{2}
\begin{aligned}
\begin{bmatrix}
1 & -i
\end{bmatrix}
^*
\begin{bmatrix}
1  \\
i
\end{bmatrix}
\end{aligned}
= 0
$$

となり直交していることが分かる。
実は任意の偏光状態は左右円偏光の重ね合わせで表すことができる。(水平偏光と垂直偏光の重ね合わせでも表現できる。)
<br>

# ジョーンズ行列
偏光素子はあるジョーンズベクトルを異なるジョーンズベクトルに変換する働きをするものだと考えるとこれは$2 \times 2$ の行列とみなせる。この行列を**ジョーンズ行列**という。

以下で説明する波長板という光学素子は遅相子(retardar)と呼ばれ、2つの直交する電場の一方の位相を変化させる。どちらの位相を遅らせるかで2通りの種類があるが
**ここでは $y$ 成分の位相が進むように( $x$ 成分の位相が遅れるように)方向を選ぶ。(yを進相軸に選ぶ。)**
**右手系か左手系か選ぶことに等しい？**
それぞれの位相を独立に変化させるので行列の非対角成分は0になると予想できる。確かに

$$
\begin{aligned}
J &=
\begin{bmatrix}
e^{i\varphi_x} & 0 \\
0 & e^{i\varphi_y}
\end{bmatrix} \\
&= e^{i\varphi_x}
\begin{bmatrix}
1 & 0 \\
0 & e^{i(\varphi_y - \varphi_x)}
\end{bmatrix} \\
&= e^{i\varphi_x}
\begin{bmatrix}
1 & 0 \\
0 & e^{i\delta}
\end{bmatrix} \\ 
\end{aligned}
$$

となる。偏光素子では位相差をどのくらい与えるのだけが重要なのであってたとえ複素数でも係数は無視していいんだと思う。つまり

$$
J =
\begin{bmatrix}
1 & 0 \\
0 & e^{i\delta}
\end{bmatrix}
$$

でいいんだと思う。
また、この行列の転置をとって複素共役をとったものと元の行列を掛けると単位行列になる。つまり偏光素子を行列で表したものは**ユニタリー行列**であることが分かる。
また、偏光子はどのくらい傾けるかによっても性質が変わり、$\theta$ だけ回転させるとジョーンズ行列は

$$
\begin{aligned}
J &=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \\
\sin{\theta} & \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
1 & 0 \\
0 & e^{i\delta}
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \\
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \\
&= 
\begin{bmatrix}
\cos{\theta} & -e^{i\delta} \sin{\theta} \\
\sin{\theta} & e^{i\delta} \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \\
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \\
\therefore J &= 
\begin{bmatrix}
e^{i\delta} \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - e^{i\delta}) \\
\sin{\theta} \cos{\theta} (1 - e^{i\delta}) & \sin^2{\theta} + e^{i\delta} \cos^2{\theta}
\end{bmatrix} \\ 
\end{aligned}
$$

となる。
これはジョーンズベクトルを回転させて偏光素子を$\theta = 0$の状態のようにし、変換されたジョーンズベクトルを元の角度に戻して完成というかんじ。考えやすい基底にしてるということ。

出力　<-　[反時計回りに $\theta$ 回転][偏光素子][時計回りに $\theta$ 回転]　<-　入力

## 1/2波長板
位相差 $\delta=\pi$ であるので

$$
\begin{aligned}
J_{HWP(\theta)} &=
\begin{bmatrix}
-\sin^2{\theta} + \cos^2{\theta} & 2\sin{\theta} \cos{\theta} \\
2\sin{\theta} \cos{\theta} & \sin^2{\theta} - \cos^2{\theta}
\end{bmatrix} \\
&= 
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \\
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

を得る。
$\theta = 0$ のときは

$$
J_{HPW(\theta=0)} =
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

というジョーンズ行列を得る。
***線形写像とかか***
例えば $\frac{\pi}{4}$ だけ傾いた直線偏光

$$
\boldsymbol{E}_{in} = \frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

を入射させると

$$
\boldsymbol{E}_{out} =\frac{e^{i\varphi_x}}{\sqrt{2}}
\begin{bmatrix}
1 \\
-1
\end{bmatrix}
$$
これは確かに $-\frac{\pi}{4}$ だけ傾いた直線偏光を表していて元の状態から時計回りに $2 \times \frac{\pi}{4}$ だけ回転している。

となる。
また、$\theta = \frac{\pi}{4}$ だけ回転させると

$$
J_{HWP(\theta=\frac{\pi}{4})} =
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$

となり**x,y成分を交換する。**

## 1/4波長板
位相差 $\delta=\frac{\pi}{2}$ であるので

$$
J_{QWP(\theta)} =
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{\theta}\\
-i\sin{\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
$$

を得る。
 $\theta = 0$ のときは

$$
J_{QWP(\theta=0)} =
\begin{bmatrix}
1 & 0 \\
0 & i
\end{bmatrix}
$$

例えば $\frac{\pi}{4}$ だけ傾いた直線偏光

$$
\boldsymbol{E}_{in} = \frac{1}{\sqrt{2}} e^{i \varphi_x}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

を入射させると

$$
\boldsymbol{E}_{out} =\frac{1}{\sqrt{2}} e^{i \varphi_x}
\begin{bmatrix}
1 \\
i
\end{bmatrix}
$$

となりこれは右回り円偏光を表している。

## SLM
$$
J_{SLM} = A_0
\begin{bmatrix}
-e^{i\delta} & 0 \\
0 & 1
\end{bmatrix}
$$

ここで
- $\delta = 2[n_e(V)-n_o]kd$
- $A_0 = e^{i2n_okd}$
- $k = \frac{2\pi}{\lambda}$
- $n_o:$光軸に垂直な面の屈折率
- $n_e:$光軸に平行な面の屈折率でこれは電圧によって制御できる

ジョーンズベクトルでこの変換の過程を表す。
⓵レーザー光がHWP,PBSによって変換される
⓶SLM1で反射してBSに戻ってくるビーム
⓷HWPを通過してSLM2で反射してHWPを通過してBSに戻ってくるビーム
⓸各SLMで反射して戻ってきたビームがBSで合わさったビーム
⓹合わさったビームがQWPで変換されたビーム

$$
\boldsymbol{E}_{out} = J_{QWP(\gamma)} [J_{SLM1} + J_{HWP(-\beta)} J_{SLM2} J_{HWP(\beta)}] J_{PBS} J_{HWP(\alpha)} \boldsymbol{E}_{in}
$$

<br>

# 偏光子とポアンカレ球
偏光成分を測るためには$E_x,E_y$が必要だが現実ではこれらの時間平均のみ計測可能である。
これらを用いると**ストークスパラメーター**というパラメーターを定義できる。

$$
\begin{align}
S_0 &= |E_x|^2 + |E_y|^2 \\
S_1 &= |E_x|^2 - |E_y|^2 \\
S_2 &= \frac{1}{2}(|E_x + E_y|^2 - |E_x - E_y|^2) \\
&= E_x^*E_y + E_x^*E_y \\
S_3 &= \frac{1}{2}(|E_x + iE_y|^2 - |E_x - iE_y|^2) \\
&= -i(E_x^*E_y - E_x^*E_y)
\end{align}
$$

これらをならべたものは**ストークスベクトル**といい

$$
\boldsymbol{S} = 
\begin{bmatrix}
A^2_x + A^2_y \\
A^2_x - A^2_y \\
2A_x A_y \cos{\delta} \\
-2A_x A_y \sin{\delta}
\end{bmatrix}
$$

と表す。
ここで $A_x, A_y$ は $x,y$ 成分の振幅で $\delta$ は $y$ 成分から見て $x$ 成分の位相のずれを表している。

偏光の軌跡は楕円偏光を考えればいい(直線を完璧な楕円、円をまったく楕円ではないものと考える)ので楕円を表すパラメーターを決めればいい。具体的には
- $\chi:$楕円率角(どのくらい楕円っぽいか)
- $\psi:$方位角(楕円がどのくらい傾いているか)

のちに導出するがこれは $S1, S2, S3$ という変数を用いて

光学の教科書ではストークスパラメータは以上のように定義されたものとして紹介される。(観測範囲ではすべての教科書でそうだった。)
そこでこれを導出する。
## 射影演算子
ジョーンズベクトルは複素ベクトルであるがストークスパラメーターは実数であるので複素数の世界から実数の世界に行く必要がある。

$$
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix} \; \alpha , \beta \in \mathbb{C}
$$

もし

$$
| \alpha | ^2 + | \beta | ^2 = 1
$$

ならば

$$
P = 
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^*
$$

が射影演算子となる。
ただしどんな行列も射影演算子となるわけではなく以下の2つを満たす必要がある。(線形写像となる条件？)

$$
\begin{aligned}
・
P^2 &= 1 \\
・
P^ \dagger &= P
\end{aligned}
$$

計算してみると

$$
\begin{aligned}
P^2 &= (
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix} 
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^* ) (
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^* ) \\
&= 
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix} (
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^*  
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix} )
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^*
\\
&= 
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix} (
| \alpha | ^2 + | \beta | ^2 )
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^* \\
\therefore P^2 &= P
\end{aligned}
$$

次に

$$
\begin{aligned}
P ^ \dagger &= (
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^* ) ^ \dagger \\
&= (
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^* ) ^ \dagger \\
&= (
\begin{bmatrix}
\alpha \\
\beta 
\end{bmatrix} ^*) ^*
\begin{bmatrix}
\alpha \; \;
\beta 
\end{bmatrix} ^* \\
\therefore P ^ \dagger &= P
\end{aligned}
$$

## パウリ行列展開
https://electrodynamics.hatenablog.com/entry/2018/12/01/233744
https://electrodynamics.hatenablog.com/entry/2018/12/16/000833

## ポアンカレ球

波長板にはかりが通ると光の偏光分布が変わるがこれはポアンカレ球面上で別の座標に写ることを表している。このように長さを変えない(今は球の表面上で移動する)写像を等長写像という。

偏光板を行列表示(ジョーンズ行列)したとき、この行列はユニタリー行列(転置とって複素共役とった行列が元の行列の逆行列になっている)であるがユニタリー行列であることが必要条件であることは確実。

長さを変えない写像というのは回転とか平行移動

## 高次元ポアンカレ球

# ブロッホ球
## 高次元ブロッホ球

# 論文解説
## SLM2個使ってベクトルビームを作る
### "Polarization distribution control of parallel femtosecond pulses with spatial light modulators"

$$
\begin{aligned}
\boldsymbol{E}_{out} &=
J_{QWP(\frac{\pi}{4})} J_{SLM2(\beta)} J_{HWP(\frac{\pi}{8})} J_{SLM1(\alpha)} \boldsymbol{E}_{in}
\\
&\propto
\begin{bmatrix}
1+i & 1-i \\
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{-i\beta} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\begin{bmatrix}
1 \\
0
\end{bmatrix} \\
&=
\begin{bmatrix}
1+i & 1-i \\
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{-i\beta} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \\
1 
\end{bmatrix} \\
&=
\begin{bmatrix}
1+i & 1-i \\
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{-i\beta} \\
1 
\end{bmatrix} \\
&=
\begin{bmatrix}
e^{-i\beta}(1+i) + 1-i \\
e^{-i\beta}(1-i) + 1+i
\end{bmatrix} \\
&=
\begin{bmatrix}
\cos{\beta} + \sin{\beta} + 1 \\
\cos{\beta} - \sin{\beta} + 1
\end{bmatrix}
+i
\begin{bmatrix}
\cos{\beta} - \sin{\beta} - 1 \\
-(\cos{\beta} + \sin{\beta} - 1)
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &=
\begin{bmatrix}
\cos{\frac{\beta}{2}} + \sin{\frac{\beta}{2}} \\
\cos{\frac{\beta}{2}} - \sin{\frac{\beta}{2}}
\end{bmatrix}
+i
\begin{bmatrix}
\cos{\frac{\beta}{2}} - \sin{\frac{\beta}{2}} - 2 \\
-(\cos{\frac{\beta}{2}} + \sin{\frac{\beta}{2}} - 2)
\end{bmatrix} \\
\therefore Re(\boldsymbol{E}_{out}) &=
\begin{bmatrix}
\cos{\frac{\beta}{2}} + \sin{\frac{\beta}{2}} \\
\cos{\frac{\beta}{2}} - \sin{\frac{\beta}{2}}
\end{bmatrix}
\end{aligned}
$$

$$
\beta = 2\varphi + \theta
$$

とすると

$$
\begin{aligned}
\boldsymbol{E}_{out} &\propto
\begin{bmatrix}
\cos{(\frac{2\varphi + \theta}{2})} + \sin{(\frac{2\varphi + \theta}{2})} \\
\cos{(\frac{2\varphi + \theta}{2})} - \sin{(\frac{2\varphi + \theta}{2})}
\end{bmatrix} \\
&=
\begin{bmatrix}
\cos{(\varphi + \frac{\theta}{2})} + \sin{(\varphi + \frac{\theta}{2})} \\
\cos{(\varphi + \frac{\theta}{2})} - \sin{(\varphi + \frac{\theta}{2})}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &\propto
\begin{bmatrix}
\cos{\varphi}(\cos{\frac{\theta}{2}} + \sin{\frac{\theta}{2}}) + \sin{\varphi}(\cos{\frac{\theta}{2}} - \sin{\frac{\theta}{2}}) \\
\cos{\varphi}(\cos{\frac{\theta}{2}} - \sin{\frac{\theta}{2}}) - \sin{\varphi}(\cos{\frac{\theta}{2}} + \sin{\frac{\theta}{2}})
\end{bmatrix}
\end{aligned}
$$

もし$\theta = -\frac{\pi}{2}$なら

$$
\begin{aligned}
\boldsymbol{E}_{out} &\propto
\begin{bmatrix}
\cos{\varphi}(\cos{\frac{\pi}{4}} - \sin{\frac{\pi}{4}}) + \sin{\varphi}(\cos{\frac{\pi}{4}} + \sin{\frac{\pi}{4}}) \\
\cos{\varphi}(\cos{\frac{\pi}{4}} + \sin{\frac{\pi}{4}}) - \sin{\varphi}(\cos{\frac{\pi}{4}} - \sin{\frac{\pi}{4}})
\end{bmatrix} \\
&\propto
\begin{bmatrix}
\sin{\varphi} \\
\cos{\varphi}
\end{bmatrix}
\end{aligned}
$$

### "Holographic femtosecond laser manipulation for advanced material processing"

$$
\boldsymbol{E}_{out} \propto 
\begin{bmatrix}
-i\cos{\beta} + \sin{\beta} + 1 \\
-\cos{\beta} -i\sin{\beta} + i
\end{bmatrix}
$$

$\beta = \varphi + \theta$とすると

$$
\begin{aligned}
\boldsymbol{E}_{out} &\propto 
\begin{bmatrix}
-i\cos{(\varphi + \theta)} + \sin{(\varphi + \theta)} + 1 \\
-\cos{(\varphi + \theta)} -i\sin{(\varphi + \theta)} + i
\end{bmatrix} \\
&\propto
\begin{bmatrix}
-i(\cos{\varphi} \cos{\theta} -\sin{\varphi} \sin{\theta}) + \sin{\varphi} \cos{\theta} + \cos{\varphi} \sin{\theta} + 1 \\
-(\cos{\varphi} \cos{\theta} -\sin{\varphi} \sin{\theta}) -i(\sin{\varphi} \cos{\theta} +\cos{\varphi} \sin{\theta})+ i
\end{bmatrix}
\end{aligned}
$$

$\beta = 2\varphi + \theta$とすると

$$
\begin{aligned}
\boldsymbol{E}_{out} &\propto 
\begin{bmatrix}
-i\cos{(2\varphi + \theta)} + \sin{(2\varphi + \theta)} + 1 \\
-\cos{(2\varphi + \theta)} -i\sin{(2\varphi + \theta)} + i
\end{bmatrix} \\
&\propto
\begin{bmatrix}
-i(\cos{2\varphi} \cos{\theta} -\sin{2\varphi} \sin{\theta}) + \sin{2\varphi} \cos{\theta} + \cos{2\varphi} \sin{\theta} + 1 \\
-(\cos{2\varphi} \cos{\theta} -\sin{2\varphi} \sin{\theta}) -i(\sin{2\varphi} \cos{\theta} +\cos{2\varphi} \sin{\theta})+ i
\end{bmatrix}
\end{aligned}
$$

ここで$\theta = \frac{\pi}{2}$とすると

$$
\boldsymbol{E}_{out} \propto
\begin{bmatrix}
i\sin{2\varphi} + \cos{2\varphi} +1 \\
\sin{2\varphi} - i\cos{2\varphi} + i
\end{bmatrix}
$$

これは

を表す。

### "Flexible generation of the generalized vector vortex beams"(2021)
得られるビームのジョーンズベクトルは以下

$$
\boldsymbol{E} = 
e^{iA\varphi}[
\cos{2\alpha}
e^{-i(B\varphi+C)}
\boldsymbol{S_1}(2\gamma, 2(2\beta-\gamma))
+\sin{2\alpha}
e^{i(B\varphi+C)}
\boldsymbol{S_2}(2\gamma+\pi, -2(2\beta-\gamma))]
$$

ただし2つのベクトル$\boldsymbol{S}$は

$$\boldsymbol{S}(2\psi, 2\chi) = 
\begin{bmatrix}
\frac{1}{\sqrt{2}}[\sin{(\chi + \frac{\pi}{4})} e^{-i\psi} + \cos{(\chi + \frac{\pi}{4}) e^{i\psi}}] \\
\frac{i}{\sqrt{2}}[\sin{(\chi + \frac{\pi}{4})} e^{-i\psi} - \cos{(\chi + \frac{\pi}{4}) e^{i\psi}}]
\end{bmatrix}
$$

SLMに表示させるホログラムは
- SLM1: $\delta_1 = p\varphi + \delta_{10}$
- SLM2: $\delta_2 = q\varphi + \delta_{20}$

パラメーターは
- $\alpha$:1つ目の半波長板を傾ける角度
- $\beta$:2つ目の半波長板を傾ける角度
- $\gamma$:4分の1波長板を傾ける角度
- $\boldsymbol{S_i}(i \in 1, 2)$は互いに直交するベクトル、**波長板を傾けるということは直交基底を選ぶことに対応する。**
- $A = p + \frac{q}{2}$
- $B = -\frac{q}{2}$
- $C = -\frac{2\delta_{20} + \pi}{4}$

ここで $\alpha = \frac{\pi}{8}, \beta = 0, \gamma = -\frac{\pi}{4}$ とすると

$$
\boldsymbol{S_1}(-\frac{\pi}{2}, \frac{\pi}{2}) \propto 
\begin{bmatrix}
1 \\
-i
\end{bmatrix}(右回り円偏光)
$$

$$
\boldsymbol{S_2}(\frac{\pi}{2}, -\frac{\pi}{2}) \propto 
\begin{bmatrix}
1 \\
i
\end{bmatrix}(左回り円偏光)
$$

となる。
さらに $p = 1, q = 2, \delta_{20} = -\frac{\pi}{2}$
とすると
$A = 2, B = -1, C = 0$
となるので代入すると

$$
\boldsymbol{E} = 
\sqrt{2} e^{i2\varphi}
\begin{bmatrix}
\cos{\varphi} \\
\sin{\varphi}
\end{bmatrix}
$$

$$
Re(\boldsymbol{E}) = \sqrt{2} \cos{2\varphi}
\begin{bmatrix}
\cos{\varphi}\\
\sin{\varphi}
\end{bmatrix}
\propto
\begin{bmatrix}
\cos{\varphi}\\
\sin{\varphi}
\end{bmatrix}
$$

この偏光分布が時々刻々と変化していくつまりこれに位相項 $e^{iX}$ をかけて実部を取ったものの形が偏光分布

たしかに種々の $\varphi$ に値を代入してみると

$$
\begin{aligned}
Re(\boldsymbol{E_{\varphi=0}}) &= 
\begin{bmatrix}
1 \\
0
\end{bmatrix} (水平偏光)\\
Re(\boldsymbol{E_{\varphi=\frac{\pi}{4}}}) &\propto 
\begin{bmatrix}
1 \\
1 
\end{bmatrix} (\frac{\pi}{4}傾いた直線偏光)\\
Re(\boldsymbol{E_{\varphi=\frac{\pi}{2}}}) &= 
\begin{bmatrix}
0 \\
1 
\end{bmatrix} (垂直偏光) \\
\end{aligned}
$$

今は偏光分布が中心からの距離に依存しないので結局

のような偏光分布が得られる。

次にパラメーターを変えて同じように考えてみる。
今度は $\alpha = \frac{\pi}{8}, \beta = -\frac{\pi}{4}, \gamma = -\frac{3\pi}{16}$


$$
\begin{aligned}
\boldsymbol{S_1}(-\frac{\pi}{2}, -\frac{\pi}{4}) &\propto 
\begin{bmatrix}
\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} + \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}} \\
i[\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} - \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}}]
\end{bmatrix}
\\
\boldsymbol{S_2}(\frac{\pi}{2}, \frac{\pi}{4}) &\propto 
\begin{bmatrix}
\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} + \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}} \\
i[\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} - \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}}]
\end{bmatrix}
\end{aligned}
$$


こっちは先ほどと同じで $p = 1, q = 2, \delta_{20} = -\frac{\pi}{2}$
ゆえ
$A = 2, B = -1, C = 0$ を代入

$$
\boldsymbol{E} \propto 
\begin{bmatrix}
e^{i\varphi} [\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} + \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}}] + e^{-i\varphi} [\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} + \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}}] \\
i (e^{i\varphi} [\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} - \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}}] + e^{-i\varphi} [\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} - \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}}])
\end{bmatrix}
$$

$$
\begin{aligned}
\boldsymbol{E}_{\varphi = \frac{\pi}{4}} &\propto
\begin{bmatrix}
e^{i\frac{\pi}{2}} \sin{\frac{\pi}{8}} + e^{-\frac{i\pi}{2}} \sin{\frac{3\pi}{8}} + \cos{\frac{\pi}{8}} + \cos{\frac{3\pi}{8}}\\
i[e^{i\frac{\pi}{2}} \sin{\frac{\pi}{8}} + e^{-\frac{i\pi}{2}} \sin{\frac{3\pi}{8}} - \cos{\frac{\pi}{8}} - \cos{\frac{3\pi}{8}}] 
\end{bmatrix} \\
&\propto
\begin{bmatrix}
\cos{\frac{\pi}{8}} + \cos{\frac{3\pi}{8}} + i[\sin{\frac{\pi}{8}} - \sin{\frac{3\pi}{8}}]\\
\sin{\frac{3\pi}{8}} - \sin{\frac{\pi}{8}} - i[\cos{\frac{\pi}{8}} + \cos{\frac{3\pi}{8}}] 
\end{bmatrix} \\
&\propto
\begin{bmatrix}
1.3 - i0.54 \\
0.54 - i1.3
\end{bmatrix}
\end{aligned}
$$

ここで位相項 $e^{i\theta}$ をかけて実部を取って $\theta$を $0\rightarrow 2\pi$ と変化させたときの軌跡をプロットすると

となりこのように傾いた左回りの楕円偏光が得られる。
論文中では

であり確かに $\varphi = \frac{\pi}{4}$ の位置ではこのような楕円になっている。

## ベクトルビームと機械学習
### "Machine learning-based classification of vector vortex beams"
https://blog.tsurubee.tech/entry/2022/enns-overview#%E5%8C%BB%E7%99%82%E7%94%BB%E5%83%8F

https://github.com/Chen-Cai-OSU/awesome-equivariant-network

https://ds-notes.com/%E5%90%8C%E5%A4%89%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF%E3%81%AE%E8%A7%A3%E8%AA%AC%EF%BC%9A%E3%81%9D%E3%81%AE-%EF%BC%91-%E7%BE%A4/

手書きの数字を見分けるという課題を考えた時に同じ数字を描いたものでもちょっとだけずれたものは画素値の場所もずれてしまうので別の画像と認識してしまう。(おんなじ数字を表しているのに。)
これを解決するために畳み込みという操作を行うことにより領域で画像を見ることによって画素値の平行移動について同じものであるとみなす。**(最後にプーリングを行わない場合)**
これは **畳み込みをしたとに平行移動させたもの、と平行移動した後に畳み込みをしたものを同一とみなすということ。**

ここで以下を満たすとき

変換 $\Phi$ と変換 $g$ は **同変:eqvariant** である、と言う。
また、変換 $\pi(g)$ が恒等写像、つまり $\pi(g) = g$ であるとき変換 $\Phi$ と変換 $g$ は **不変:variant** である、という。

## ベクトルビームと幾何学
### "Observation of optical polarization Möbius strips"

### "Full Poincare´ beams"
### "Generation of A Space-Variant Vector Beam with Catenary-Shaped Polarization States"

## Gouy位相
### パンチャラトナムベリー位相
### "光学におけるベリー位相"
### "Manifestation of the Gouy phase in strongly focused, radially polarized beams" 

## 高次元ポアンカレ球
### "Higher-Order Poincaré Sphere, Stokes Parameters, and the Angular Momentum of Light"
### "Generalized Poincare sphere"

## ベクトルビームの評価方法
### "Measuring the nonseparability of vector vortex beams"
### "Beam quality measure for vector beams"
### "ENTANGLEMENT OF FORMATION AND CONCURRENCE"

## 近軸近似のもとでスカラー場に対するヘルムホルツ方程式を解く
### "From Maxwell to paraxial wave optics"
### "Gaussian Beam 計算メモ"
### HGbeam
http://solidstatephysics.blog.fc2.com/blog-entry-47.html
### LGbeam

### ヘルムホルツ方程式の導出

ファラデーの法則

$$
\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) = -\frac{\partial \boldsymbol {B} (\boldsymbol {r} , t) } {\partial t}
$$

に対して両辺の回転を取ると

$$
\nabla \times (\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) ) = - \mu_0 \nabla \times \frac{\partial \boldsymbol {H} (\boldsymbol {r} , t) }{\partial t}
$$

となるがここでアンペールの法則

$$
\nabla \times \boldsymbol {H} (\boldsymbol {r} , t) = \epsilon_0 \frac{\partial \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t}
$$

を代入すると

$$
\nabla \times (\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) ) = - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2}
$$

を得る。ここで

$$
\nabla \times (\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) ) = \nabla(\nabla \cdot \boldsymbol {E} (\boldsymbol {r} , t) ) - \nabla^2 \boldsymbol {E} (\boldsymbol {r} , t)
$$

より

$$
\nabla(\nabla \cdot \boldsymbol {E} (\boldsymbol {r} , t) ) - \nabla^2 \boldsymbol {E} (\boldsymbol {r} , t) = - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2}
$$

を得る。電荷がない場合を考えているので

$$
\nabla \cdot \boldsymbol {E} (\boldsymbol {r} , t) = 0
$$

より

$$
\begin{aligned}
- \nabla^2 \boldsymbol {E} (\boldsymbol {r} , t) &= - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2} \\
\nabla^2 \boldsymbol {E} (\boldsymbol {r} , t) &= \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2} 
\end{aligned}
$$

$$
\therefore \nabla^2 \boldsymbol{E} (\boldsymbol {r} , t) - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t)}{\partial t^2} = 0
$$

ここで解の形を

$$
\boldsymbol {E} (\boldsymbol {r} , t) = \boldsymbol {E} (\boldsymbol {r}) f(t)
$$

と分離できると仮定する。これを代入すると

$$
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) f(t) - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} ) f(t)}{\partial t^2} = 0
$$

を得る。ここでフーリエ変換

$$
F(\omega) = \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}f(t) e^{i \omega t}dt
$$

を考えると

$$
f(t) = \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega
$$

であるので代入すると

$$
\begin{aligned}
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} )}{\partial t^2} \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega + \frac{\epsilon_0 \mu_0 \omega ^2}{\sqrt{2 \pi}} \boldsymbol {E} (\boldsymbol {r} ) \int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \epsilon_0 \mu_0 \omega ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \frac{\omega ^2}{c^2} \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \biggl (\frac{2 \pi f}{f \lambda} \biggr ) ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \biggl (\frac{2 \pi}{\lambda} \biggr ) ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\therefore \nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + k ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0
\end{aligned}
$$

これはヘルムホルツ方程式と言うタイプの偏微分方程式。

もし電場がスカラー場(偏光分布が直線であるので厳密にはベクトル場であるが座標系を適当に選べば電場の大きさだけを考えればいい)であれば

$$
\boldsymbol{E}(\boldsymbol{r}) = u(x, y, z) e^{ikz} 
$$

のように書ける。これをヘルムホルツ方程式に代入すると

$$
\begin{aligned}
\Bigl (\frac{\partial ^2}{\partial ^2 x} + \frac{\partial ^2}{\partial ^2 y} + \frac{\partial ^2}{\partial ^2 z} \Bigr ) \bigl (u(x, y, z) e^{ikz} \bigr ) + k^2 u(x, y, z) e^{ikz} &= 0 \\
\Bigl (\frac{\partial ^2 u}{\partial ^2 x} + \frac{\partial ^2 u}{\partial ^2 y} + \frac{\partial ^2 u}{\partial ^2 z} + 2ik \frac{\partial u}{\partial z} - k^2 u + k^2 u \Bigr ) e^{ikz} &= 0 \\
\frac{\partial ^2 u}{\partial ^2 x} + \frac{\partial ^2 u}{\partial ^2 y} + \frac{\partial ^2 u}{\partial ^2 z} + 2ik \frac{\partial u}{\partial z} &= 0
\end{aligned}
$$

ここで近軸近似を考えると

$$
\frac{\partial ^2 u}{\partial ^2 x} + \frac{\partial ^2 u}{\partial ^2 y} + 2ik \frac{\partial u}{\partial z} = 0
$$

を得る。

## 近軸近似のもとでベクトル場に対するヘルムホルツ方程式を解く
### 参考:"Separability and Applications"
### "Vector-beam solutions of Maxwell's wave equation"
### "Vector Helmholtz–Gauss and vector Laplace–Gauss beams"
### エルミート多項式
http://solidstatephysics.blog.fc2.com/blog-entry-31.html
"腰も砕けよ 膝も折れよ"https://decafish.blog.ss-blog.jp/archive/c2305062484-1
radial polarizationやazimuthal polarizationはベクトルヘルムホルツ方程式の固有値として与えられる

### ラプラシアンを考える

演算する関数がスカラー場の時、ラプラシアンを演算するということは

$$
\nabla ^2 f = \nabla \cdot (\nabla f)
$$

となり勾配をとった後に発散をとることに相当する。**(スカラーラプラス演算子)**

演算する関数がベクトル場の時、ラプラシアンを演算するということは

$$
\nabla ^2 \boldsymbol{f} = \nabla (\nabla \cdot \boldsymbol{f})
- \nabla \times (\nabla \times \boldsymbol{f})
$$

に相当する。**(ベクトルラプラス演算子)**

今は電荷が存在しないマクスウェル方程を考えているので右辺第1項はゼロになり

$$
\nabla \times \nabla \times \boldsymbol{E} -k^2 \boldsymbol{E} = 0
$$

となる。解の形として

$$
\boldsymbol{E}(r, z) = U(r, z) e^{ikz} \boldsymbol{e}_\phi
$$

のように軸対称な解を考える。

円筒座標系でのナブラは

$$
\nabla = \frac{\partial}{\partial r} \boldsymbol{e}_r + \frac{1}{r} \frac{\partial}{\partial \phi} + \frac{\partial}{\partial z} \boldsymbol{e}_z
$$

で
であるが今は $\phi$ が一定であるので

$$
\nabla = \frac{\partial}{\partial r} \boldsymbol{e}_r + \frac{\partial}{\partial z} \boldsymbol{e}_z
$$

となる。回転をとると

$$
\nabla \times \boldsymbol{E} = \Bigl (\frac{1}{r} \frac{\partial}{\partial \phi} E_z - \frac{\partial}{\partial z} E_\phi \Bigr ) \boldsymbol{e}_r + \Bigl (\frac{\partial}{\partial z} E_r - \frac{\partial}{\partial r} E_z \Bigr ) \boldsymbol{e}_\phi + \frac{1}{r} \Bigl (\frac{\partial}{\partial r} (r E_\phi) - \frac{\partial}{\partial \phi} E_r \Bigr )\boldsymbol{e}_z
$$

であるが今は

$$
E_r = E_z = 0
$$

より

$$
\nabla \times \boldsymbol{E} = - \frac{\partial}{\partial z} E_\phi \boldsymbol{e}_r + \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \boldsymbol{e}_z
$$

$$
\begin{aligned}
\nabla \times (\nabla \times \boldsymbol{E}) &= \frac{1}{r} \frac{\partial}{\partial \phi} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \Bigr ) \boldsymbol{e}_r - \Bigl ( \frac{\partial ^2}{\partial z ^2} E_\phi + \frac{\partial}{\partial r} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \Bigr ) \Bigr ) \boldsymbol{e}_\phi \\
&= - \Bigl ( \frac{\partial ^2}{\partial z ^2} E_\phi + \frac{\partial}{\partial r} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \Bigr ) \Bigr ) \boldsymbol{e}_\phi \\
&※ E_\phi は \phi を含まないので第1項はゼロ
\end{aligned}
$$

いったん整理すると

$$
\begin{aligned}
\nabla \times \nabla \times \boldsymbol{E} - k^2 \boldsymbol{E} &= 0 \\
- \frac{\partial ^2}{\partial z ^2} E_\phi - \frac{\partial}{\partial r} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \Bigr ) - k^2 E_\phi &= 0 \\
\end{aligned}
$$

これを計算すれば

$$
\begin{aligned}
\Bigl ( - \frac{\partial ^2 U}{\partial z ^2} - 2ik \frac{\partial U}{\partial z} + k^2 U + \frac{1}{r^2} U - \frac{1}{r} \frac{\partial U}{\partial r} - \frac{\partial ^2 U}{\partial r ^2} - k^2 U \Bigr ) e^{ikz} &= 0 \\
- \frac{\partial ^2 U}{\partial z ^2} - 2ik \frac{\partial U}{\partial z} + \frac{1}{r^2} U - \frac{1}{r} \frac{\partial}{\partial r} \Bigl ( r \frac{\partial U}{\partial r} \Bigl ) &= 0 \\
\therefore \quad \frac{1}{r} \frac{\partial}{\partial r} \Bigl ( r \frac{\partial U}{\partial r} \Bigl ) - \frac{1}{r^2} U + 2ik \frac{\partial U}{\partial z} + \frac{\partial ^2 U}{\partial z ^2} &= 0
\end{aligned}
$$

を得る。例によって近軸近似をすると左辺第4項はゼロになるので

$$
\frac{1}{r} \frac{\partial}{\partial r} \Bigl ( r \frac{\partial U}{\partial r} \Bigl ) - \frac{1}{r^2} U + 2ik \frac{\partial U}{\partial z} = 0
$$

を得る。

## 近軸近似せずにスカラー場のヘルムホルツ方程式を解く

### "Nonparaxial Propagation Properties of Specially Correlated Radially Polarized Beams in Free Space"
### "Closed-form bases for the description of monochromatic, strongly focused, electromagnetic fields"
### "Measuring the nonseparability of vector vortex beams"

# 実験案
## その１

⓵,BSに入射するビーム(HWP, PBS)
レーザーから出た光のジョーンズベクトルは

$$
\boldsymbol{E} = 
\begin{bmatrix}
E_{x0} e^{i\varphi_x} \\
E_{y0} e^{i\varphi_y}
\end{bmatrix}
$$

となる。

$\alpha$ だけ傾けたHWPのジョーンズ行列は

$$
J_{HWP(\alpha)} = 
\begin{bmatrix}
\cos{2\alpha} & \sin{2\alpha} \\
\sin{2\alpha} & -\cos{2\alpha}
\end{bmatrix}
$$

となる。

今はPBSをP偏光を取り出すものとして使っているのでジョーンズ行列は

$$
J_{PBS} = 
\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
$$

となる。これらをかければよいので

$$
\vec{a}_{in} \vec{b}_{out}
$$

$$
\vec{a} \stackrel{\text{in}}{\longrightarrow} \vec{b} \stackrel{\text{out}}{\longrightarrow}
$$

$$
\vec{a}_{\text{in}} \vec{b}_{\text{out}}
$$

$$
\vec{a}_{\mathrm{in}} \vec{b}_{\mathrm{out}}
$$

$$
\vec{a}_{\text{in}} \quad \vec{b}_{\text{out}}
$$

$\vec{a}_{\text{in}}$ $\vec{b}_{\text{out}}$

$$\begin{aligned}
\vec{{E}_{aa}}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \\
\vec{E}_{aa}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \\
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\end{aligned}$$

$$\begin{aligned}
\boldsymbol{E}_{out1} &=
J_{PBS} J_{HWP(\alpha)} \boldsymbol{E}_{in} \\ &= 
\begin{bmatrix}
1 & 0 \\
0 & 0 
\end{bmatrix}
\begin{bmatrix}
\cos{2\alpha} & \sin{2\alpha} \\
\sin{2\alpha} & -\cos{2\alpha}
\end{bmatrix}
\begin{bmatrix}
E_{x0} e^{i\varphi_x} \\
E_{y0} e^{i\varphi_y}
\end{bmatrix} \\ &=
\begin{bmatrix}
\cos{2\alpha} & \sin{2\alpha} \\
0 & 0
\end{bmatrix}
\begin{bmatrix}
E_{x0} e^{i\varphi_x} \\
E_{y0} e^{i\varphi_y}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out1}&=
\begin{bmatrix}
E_{x0} e^{i\varphi_x} \cos{2\alpha} + E_{y0} e^{i\varphi_y} \sin{2\alpha} \\ 0
\end{bmatrix}
\end{aligned}$$

つまりここではP偏光成分の大きさを決めていている。
今は偏光を考えているのでここでは便宜上

$$
\boldsymbol{E}_{out1} =
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

とする。

⓶,SLM1で反射してBSに戻ってくるビーム

$$
J_{SLM} = A_0
\begin{bmatrix}
-e^{i\delta} & 0 \\
0 & 1
\end{bmatrix}
$$

であったが先ほどと同様に強度の情報はいらないので今は

$$
J_{SLM1} = 
\begin{bmatrix}
-e^{i\delta_1} & 0 \\
0 & 1
\end{bmatrix}
$$

$\delta_1 = p\varphi + \delta_{10} \quad (p \in \mathbb{Z})$

$$
J_{SLM2} = 
\begin{bmatrix}
-e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
$$

$\delta_2 = q\varphi + \delta_{20} \quad (q \in \mathbb{Z})$

- $\varphi:$ 方位角(azimuthal angle)
- $\delta_{10}, \delta_{20}:$ constant phase

とする。(軸対称なベクトルビームを作りたいので変数は $\varphi$ (方位角のみ))
よってSLM1で反射してBSに戻ってくるビームは

$$
\begin{aligned}
\boldsymbol{E}_{out2} &=
\begin{bmatrix}-e^{i\delta_1} & 0 \\
0 & 1\end{bmatrix}\boldsymbol{E}_{out1} \\ 
\boldsymbol{E}_{out2} &=
\begin{bmatrix}-e^{i\delta_1} & 0 \\
0 & 1\end{bmatrix}\begin{bmatrix}1 \\
0\end{bmatrix} \\
\therefore \boldsymbol{E}_{out2} &=
\begin{bmatrix} -e^{i\delta_1} \\ 
0
\end{bmatrix}
\end{aligned}
$$

これも偏光だけを考えているので

$$
\boldsymbol{E}_{out2} = 
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

SLM1の役割は波面変調

⓷, $\beta$ 傾けたHWPを通過してSLM2で反射して先ほどと同じHWPを通過してBSに戻ってくるビーム

$$
\begin{aligned}
\boldsymbol{E}_{out3} &=
J_{HWP(-\beta)} J_{SLM2} J_{HWP(\beta)} \boldsymbol{E}_{out1}\\
&=
\begin{bmatrix}
\cos{2\beta} & -\sin{2\beta} \\
-\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
-e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} & \sin{2\beta} \\
\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
1 \\
0 
\end{bmatrix} \\
&=
\begin{bmatrix}
\cos{2\beta} & -\sin{2\beta} \\
-\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
-e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} \\
\sin{2\beta}
\end{bmatrix} \\
&=
\begin{bmatrix}
\cos{2\beta} & \sin{2\beta} \\
\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
-e^{i\delta_2}\cos{2\beta} \\
\sin{2\beta}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out3} &=
\begin{bmatrix} 
-e^{i\delta_2} \cos^2{2\beta} + \sin^2{2\beta} \\
-\frac{e^{i\delta_2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix}
\end{aligned}
$$

⓸各SLMで反射して戻ってきたビームがBSで合わさったビーム

$$
\begin{aligned}
\boldsymbol{E}_{out4} &= \boldsymbol{E}_{out2} + \boldsymbol{E}_{out3} \\
&=
\begin{bmatrix}
1 \\
0
\end{bmatrix} + 
\begin{bmatrix}
-e^{-i\delta_2} \cos^2{2\beta} - \sin^2{2\beta} \\
-\frac{e^{-i\delta_2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out4} &= 
\begin{bmatrix}
1 -e^{-i\delta_2} \cos^2{2\beta} + \sin^2{2\beta}\\
-\frac{e^{-i\delta_2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix}
\end{aligned}
$$

⓹,⓸のビームが $\gamma$ 傾けたQWPで変換されたビーム

$$
\begin{aligned}
\boldsymbol{E}_{out} &=
J_{QWP(\gamma)} \boldsymbol{E}_{out4}\\
&=
\begin{bmatrix}
i \sin^2{\gamma} + \cos^2{\gamma} & \sin{\gamma} \cos{\gamma} (1 - i) \\
\sin{\gamma} \cos{\gamma} (1 - i) & \sin^2{\gamma} + i \cos^2{\gamma}
\end{bmatrix}
\begin{bmatrix}
1 -e^{-i\delta_2} \cos^2{2\beta} + \sin^2{2\beta} \\
-\frac{e^{-i\delta_2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix} \\
&=
\begin{bmatrix}
(1 -e^{-i\delta_2} \cos^2{2\beta} + \sin^2{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + (-\frac{e^{-i\delta_2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}) (\sin{\gamma} \cos{\gamma} (1 - i)) \\
(1 -e^{-i\delta_2} \cos^2{2\beta} + \sin^2{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) + (-\frac{e^{-i\delta_2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}) (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix}
\end{aligned}
$$

天下り的に軸対称ビームを作るとき $\beta, \gamma$ をどうすればいいか考える。
例えば

$$
\boldsymbol{a} = e^{i\theta}
\begin{bmatrix}
\cos{\varphi} \\
\sin{\varphi}
\end{bmatrix}
$$

というジョーンズベクトルを考えるとこれは各 $\varphi$ で半径方向を向く直線偏光を表している。今は半径:r=1とすると
偏光分布は以下のようになる。

また

$$
\boldsymbol{b} = e^{i\theta}
\begin{bmatrix}
-\sin{\varphi} \\
\cos{\varphi}
\end{bmatrix}
$$

というジョーンズベクトルは各 $\varphi$ で円の接線方向を向く直線偏光を表している。また、半径方向には依存性はないので偏光分布は以下のようになる。

今は一つ目の偏光分布を作ることを考える。

解くのは

$$
\begin{aligned}
Re[(1 -e^{i\delta_2} \cos^2{2\beta} - \sin^2{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + \frac{\sin4\beta}{2}(-e^{i\delta_2} + 1) (\sin{\gamma} \cos{\gamma} (1 - i))] &= \cos{\varphi} \\
Re[(1 -e^{i\delta_2} \cos^2{2\beta} - \sin^2{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) + \frac{\sin{4\beta}}{2}(-e^{i\delta_2} + 1) (\sin^2{\gamma} + i \cos^2{\gamma})] &= \sin{\varphi}
\end{aligned}
$$

まず

$$
\delta_2 = 2\varphi - \frac{\pi}{2}
$$

と仮定する。第一式は

$$
Re[(1 - \sin{2\varphi} \cos^2{2\beta} - \sin^2{2\beta} -i\cos{2\varphi} \cos^2{2\beta}) (i\sin^2{\gamma} + \cos^2{\gamma}) + \frac{\sin{4\beta}}{2} (1 - \sin{2\varphi} - i\cos{2\varphi})]
$$

<br>

**[補足]**
もしSLM2に入射するビームのところのHWPが1回だけしか通らないとしたら

$$
\boldsymbol{E}_{out} = J_{QWP(\gamma)} [J_{SLM1} + J_{SLM2} J_{HWP(\beta)}] J_{PBS} J_{HWP(\alpha)} \boldsymbol{E}_{in}
$$

となるので

$$
\begin{aligned}
\boldsymbol{E}_{out3} &=
J_{SLM2} J_{HWP(\beta)} \boldsymbol{E}_{out1}\\
&=
\begin{bmatrix}
-e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} & \sin{2\beta} \\
\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
1 \\
0 
\end{bmatrix} \\
&=
\begin{bmatrix}
-e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} \\
\sin{2\beta}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out3} &=
\begin{bmatrix} 
-e^{i\delta_2} \cos{2\beta} \\
\sin{2\beta}
\end{bmatrix}
\end{aligned}
$$

となり

$$
\begin{aligned}
\boldsymbol{E}_{out4} &= \boldsymbol{E}_{out2} + \boldsymbol{E}_{out3} \\
&=
\begin{bmatrix}
1 \\
0
\end{bmatrix} + 
\begin{bmatrix} 
-e^{-i\delta_2} \cos{2\beta} \\
\sin{2\beta}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out4} &=
\begin{bmatrix}
1 -e^{-i\delta_2} \cos{2\beta}\\
\sin{2\beta}
\end{bmatrix}
\end{aligned}
$$

$$
\begin{aligned}
\boldsymbol{E}_{out} &=
J_{QWP(\gamma)} \boldsymbol{E}_{out4}\\
&=
\begin{bmatrix}
i \sin^2{\gamma} + \cos^2{\gamma} & \sin{\gamma} \cos{\gamma} (1 - i) \\
\sin{\gamma} \cos{\gamma} (1 - i) & \sin^2{\gamma} + i \cos^2{\gamma}
\end{bmatrix}
\begin{bmatrix}
1 -e^{-i\delta_2} \cos{2\beta}\\
\sin{2\beta}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &=
\begin{bmatrix}
(1 -e^{-i\delta_2} \cos{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + \sin{2\beta} (\sin{\gamma} \cos{\gamma} (1 - i)) \\
(1 -e^{-i\delta_2} \cos{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) +\sin{2\beta} (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix}
\end{aligned}
$$

ここで

$$
\delta_2 = 2\varphi + \theta
$$

とすると

$$
\begin{aligned}
\therefore \boldsymbol{E}_{out} &=
\begin{bmatrix}
(1 -\cos{(2\varphi + \theta)} -i\sin{(2\varphi + \theta)} \cos{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + \sin{2\beta} (\sin{\gamma} \cos{\gamma} (1 - i)) \\
(1 -\cos{(2\varphi + \theta)} -i\sin{(2\varphi + \theta)} \cos{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) +\sin{2\beta} (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix} \\
&=
\begin{bmatrix}
(1 - \cos{2\varphi} \cos{\theta} + \sin{2\varphi} \sin{\theta} -i \cos{2\beta} (\sin{2\varphi} \cos{\theta} + \cos{2\varphi} \sin{\theta})) (i \sin^2{\gamma} + \cos^2{\gamma}) + \sin{2\beta} (\sin{\gamma} \cos{\gamma} (1 - i)) \\
(1 - \cos{2\varphi} \cos{\theta} + \sin{2\varphi} \sin{\theta} -i \cos{2\beta} (\sin{2\varphi} \cos{\theta} + \cos{2\varphi} \sin{\theta})) (\sin{\gamma} \cos{\gamma} (1 - i)) +\sin{2\beta} (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix} \\
\end{aligned}
$$

## その２

これは

$$
\boldsymbol{E}_{out} = J_{QWP(\gamma)} J_{HWP(-\beta)} J_{SLM2(\delta_2)} J_{HWP(\beta)} J_{SLM1(\delta_1)}J_{PBS} J_{HWP(\alpha)} \boldsymbol{E}_{in}
$$

## その３

$$
\boldsymbol{E}_{out} = J_{QWP(\frac{\pi}{4})} (J_{SLM1} \boldsymbol{E}_{1} + J_{HWP(-\frac{\pi}{4})} J_{SLM2} J_{HWP(\frac{\pi}{4})} \boldsymbol{E}_{2}) \\
(\boldsymbol{E}_{in} = \boldsymbol{E}_{1} + \boldsymbol{E}_{2})
$$

今は $PBS$ によって

$$
\boldsymbol{E}_{in} = \boldsymbol{E}_{1} + \boldsymbol{E}_{2} = 
\begin{bmatrix}
1 \\
0
\end{bmatrix}
+
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

と分けられる。よって

$$
\begin{aligned}
\boldsymbol{E}_{out} &= J_{QWP(\frac{\pi}{4})} (J_{SLM1} 
 \begin{bmatrix}
1 \\
0
\end{bmatrix} + J_{HWP(-\frac{\pi}{4})} J_{SLM2} J_{HWP(\frac{\pi}{4})} \begin{bmatrix}
0 \\
1
\end{bmatrix}
) \\
&=
\begin{bmatrix}
1 & -i \\
-i & 1
\end{bmatrix} \biggl(
\begin{bmatrix}
e^{i\delta_1} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \\
0 
\end{bmatrix}
+\begin{bmatrix}
0 & -1 \\
-1 & 0
\end{bmatrix}
\begin{bmatrix}
e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
\begin{bmatrix}
0 \\
1
\end{bmatrix} \biggr) \\
&=
\begin{bmatrix}
1 & -i \\
-i & 1
\end{bmatrix} \biggl(
\begin{bmatrix}
e^{i\delta_1} \\
0 
\end{bmatrix}
+\begin{bmatrix}
0 & -1 \\
-1 & 0
\end{bmatrix}
\begin{bmatrix}
e^{i\delta_2} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \\
0
\end{bmatrix} \biggr) \\
&=
\begin{bmatrix}
1 & -i \\
-i & 1
\end{bmatrix} \biggl(
\begin{bmatrix}
e^{i\delta_1} \\
0 
\end{bmatrix}
+\begin{bmatrix}
0 & -1 \\
-1 & -0
\end{bmatrix}
\begin{bmatrix}
e^{i\delta_2} \\
0
\end{bmatrix}
 \biggr)
 \\
&=
\begin{bmatrix}
1 & -i \\
-i & 1
\end{bmatrix} \biggl(
  e^{i\delta_1}
\begin{bmatrix}
1 \\
0 
\end{bmatrix}
+e^{i\delta_2}
\begin{bmatrix}
0 \\
1
\end{bmatrix}
 \biggr)
  \\
&=
  e^{i\delta_1}
\begin{bmatrix}
1 \\
-i 
\end{bmatrix}
+e^{i\delta_2}
\begin{bmatrix}
-i \\
1
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &=
  e^{i\delta_1}
\begin{bmatrix}
1 \\
-i 
\end{bmatrix}
+e^{i\delta_2}
\begin{bmatrix}
1 \\
i
\end{bmatrix}
\end{aligned}
$$

このように位相変調された左右円偏光の重ね合わせで表現される。

ここで

$$
\begin{aligned}
\delta_{1} &= \phi + \phi_{0} \\
\delta_{2} &= -(\phi + \phi_{0})
\end{aligned}
$$

という位相をSLMに表示させることを考える。
例えば

$$
\begin{aligned}
\delta_1 &= \phi \\
\delta_2 &= -\phi
\end{aligned}
$$

とすると

$$
\begin{aligned}
\boldsymbol{E}_{out} &= e^{i\phi}
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+e^{-i\phi}
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&= (\cos{\phi} + i\sin{\phi})
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+(\cos{\phi} - i\sin{\phi})
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&=
\begin{bmatrix}
\cos{\phi} + i\sin{\phi} \\
\sin{\phi} - i\cos{\phi}
\end{bmatrix}+
\begin{bmatrix}
\cos{\phi} - i\sin{\phi} \\
\sin{\phi} + i\cos{\phi}
\end{bmatrix} \\
&=
\begin{bmatrix}
2\cos{\phi} \\
2\sin{\phi}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &\propto
\begin{bmatrix}
\cos{\phi} \\
\sin{\phi}
\end{bmatrix}
\end{aligned}
$$

これは各 $\phi$ でその点と原点を結ぶ方向の直線偏光を表している。
つまり中心から外側に向かうような偏光分布になる。

$(\cos{\phi}, \sin{\phi})$ の点でのベクトル $\boldsymbol{E}_{out}$ をプロットしたもの

次に

$$
\begin{aligned}
\delta_1 &= \phi + \frac{\pi}{2}\\
\delta_2 &= -(\phi + \frac{\pi}{2})
\end{aligned}
$$

とすると

$$
\begin{aligned}
\boldsymbol{E}_{out} &= e^{i(\phi + \frac{\pi}{2})}
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+e^{-i(\phi + \frac{\pi}{2})}
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&= \Bigl( \cos{(\phi + \frac{\pi}{2})} + i\sin{(\phi + \frac{\pi}{2})} \Bigr)
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+\Bigl(\cos{(\phi + \frac{\pi}{2})} - i\sin{(\phi + \frac{\pi}{2})} \Bigr)
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&= \Bigl( -\sin{\phi} + i\cos{\phi} \Bigr)
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+\Bigl(-\sin{\phi} - i\cos{\phi} \Bigr)
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&=
\begin{bmatrix}
-\sin{\phi} + i\cos{\phi} \\
\cos{\phi} + i\sin{\phi}
\end{bmatrix}+
\begin{bmatrix}
-\sin{\phi} - i\cos{\phi} \\
\cos{\phi} - i\sin{\phi}
\end{bmatrix} \\
&=
\begin{bmatrix}
-2\sin{\phi} \\
2\cos{\phi}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &\propto
\begin{bmatrix}
\sin{\phi} \\
-\cos{\phi}
\end{bmatrix}
\end{aligned}
$$

これは各 $\phi$ で円の接線方向を向いた直線偏光を表している。確かに

$$
\begin{bmatrix}
\cos{\phi} \\
\sin{\phi}
\end{bmatrix} \cdot
\begin{bmatrix}
\sin{\phi} \\
-\cos{\phi}
\end{bmatrix} = 0
$$

直交している。

$(\cos{\phi}, \sin{\phi})$ の点でのベクトル $\boldsymbol{E}_{out}$ をプロットしたもの

最後に

$$
\begin{aligned}
\delta_1 &= 2\phi \\
\delta_2 &= -2\phi
\end{aligned}
$$

を考える。

$$
\begin{aligned}
\boldsymbol{E}_{out} &= e^{i2\phi}
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+e^{-i2\phi}
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&= (\cos{2\phi} + i\sin{2\phi})
\begin{bmatrix}
1 \\
-i
\end{bmatrix}
+(\cos{2\phi} - i\sin{2\phi})
\begin{bmatrix}
1 \\
i
\end{bmatrix} \\
&=
\begin{bmatrix}
\cos{2\phi} + i\sin{2\phi} \\
\sin{2\phi} - i\cos{2\phi}
\end{bmatrix}+
\begin{bmatrix}
\cos{2\phi} - i\sin{2\phi} \\
\sin{2\phi} + i\cos{2\phi}
\end{bmatrix} \\
&=
\begin{bmatrix}
2\cos{2\phi} \\
2\sin{2\phi}
\end{bmatrix} \\
\therefore \boldsymbol{E}_{out} &\propto
\begin{bmatrix}
\cos{2\phi} \\
\sin{2\phi}
\end{bmatrix}
\end{aligned}
$$

$(\cos{\phi}, \sin{\phi})$ の点でのベクトル $\boldsymbol{E}_{out}$ をプロットしたもの

# 教科書的な立ち位置

## ベクトルビーム
### "Cylindrical vector beams: from mathematical concepts to applications"
### "Vector Beams for Fundamental Physics and Applications"
## 光渦
### "Orbital angular momentum: origins, behavior and applications"
## SLM
### "Creation and detection of optical modes with spatial light modulators"

![Alt text](images/image.png)