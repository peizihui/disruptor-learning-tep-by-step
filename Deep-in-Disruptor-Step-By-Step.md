Deep-in-Disruptor-Step-By-Step

# 1. 概览









# 2. Disruptor Quick Start

## 2.1 建立Event类



**建立一个工厂Event类，用于创建Eveent类实例对象**

```
package com.wisdom.disruptor.quickstart;

public class OrderEvent {

    public long getValue() {
        return value;
    }

    public void setValue(long value) {
        this.value = value;
    }

    private long value;

}
```



##2.2  创建事件监听类

**需要一个事件监听类，用于处理数据(Event类)**

```
package com.wisdom.disruptor.quickstart;
import com.lmax.disruptor.EventHandler;

/**
 *  具体消费者，
 */
public class OrderEventHandler implements  EventHandler<OrderEvent> {
    /**
     *事件驱动时间，
     */
    @Override
    public void onEvent(OrderEvent orderEvent, long l, boolean b) throws Exception {
        System.out.println("OrderEventHandler.onEvent value =="+orderEvent.getValue());
    }
}
```





## 2.3  实例化Disruptror实例

**实例化Disruptror实例，配置一系列参数，编写Disruptor核心组件**









## 2.4 编写生产者组件





