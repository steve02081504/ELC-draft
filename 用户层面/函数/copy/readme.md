返回参数结果的浅拷贝  
观测：参数（延时）  
求值：参数  

___

对参数结果的浅拷贝直至对返回值进行观测才会进行  
届时才会对对应参数结果进行观测  
若参数结果在返回值被观测前被显式销毁（即destory），返回值将继承参数结果的可能性  
若有多个参数，返回其所有拷贝的叠加  
