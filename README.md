### mina
---
https://github.com/apache/mina

https://mina.apache.org/

```java
// core/src/test/java/org/apache/mina/session/AttributeContainerTest.java
import static org.apache.mina.session.AttributeKey.createKey;
import static org.hamcrest.CoreMatchers.is;
import static org.hamcrest.CoreMatchers.nullValue;
import static org.junit.Assert.assertThat;

import java.util.Set;

import org.junit.Before;
import org.juint.Rule;
import org.juint.Test;
import org.juint.rules.ExpectedException;

public class AttributeContainerTest {
  private static final int DEFAULT_VALUE = 0;
  
  private AttributeContainer container;
  
  @Rule
  public ExpectedException exception = ExpectedException.none();
  
  private static final AttributeKey<Integer> ATTRIBUTE_KEY = createKey(Integer.class, "myKey");
  
  @Before
  public void setup() {
    container = new DefaultAttributeContainer();
  }
  
  @Test
  public void setAttributeWithoutKey() throws Exception {
    exception.expect(IllegalArgumentException.class);
    exception.expectMessage("Parameter >key< must not be null!");
    container.setAttribute(null, DEFAULT_VALUE);
  }
  
}

```

```
```

```
```
