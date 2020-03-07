# chigua
http://cfd-china.com/topic/3322/les%E5%88%9D%E5%A7%8B%E9%80%9F%E5%BA%A6%E5%9C%BA%E8%AE%BE%E7%BD%AE%E5%92%8C%E5%A3%81%E9%9D%A2%E5%87%BD%E6%95%B0%E8%AE%BE%E7%BD%AE/16


> 上次算到step2的中心差分的50.5s处，说可能会阻力又下降。

建议楼主定一个准则.比如计算了 N 个 Vortex Shedding 周.之后又计算了 2N
个周期,然后比较一下所感兴趣的物理量.


> 那之后我把它继续算到了59.5s，然后速度对流项的linear换到了
> limitedLinear。把结果贴上来一下。


不清楚楼主研究的重点是?层主个人来说,是很好奇, linear -> limitedLinear
的区别.


> 整体看起来的话，三个阶段的定量CdCl差距不是很大。和文献也对的比较上。
> 初 步认定是速度对流项选择了迎风格式造成的。跟之前的猜想有关，在55s处残
> 差的Uy震荡明显，造成了Cd上升，Cl振幅也增大. 换成limitedLinear 0.5 之后，
> 可以发现残差有明显的下降。

不知楼主有没有对这些格式的比较?

UDS 对网格要求更高.

"Peaks or rapid variations in the variables will be smeared out and,
because the rate of error reduction is only first order,
**very fine** grids are required to obtain accurate solutions."

楼主还可以探索一下这些:

- Linear Interpolation (CDS)
- Quadratic Upwind Interpolation (QUICK)
- Higher-Order Schemes


> @random_ran 是否可以回答前面的问题，虽然P的量级并没有发生变化。但是Uz
> 的曲线震荡明显（相比中心差分），猜想可能是由于TVD 里头那个0.5造成的，
> 混入了一部分迎风格式，造成耗散？

我没法准确回答你,因为我自己没有太多探索过.


> 我这样中途切换差分格式是否ok？

为什么不可以?如果是研究格式的问题,我可能也会这么做,省很多时间.但是如果
是分析流体机理,最好从头开始用一种固定格式.



