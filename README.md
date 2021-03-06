### fast or slow, soon or later

```java
public int medium() {
    Node slowPtr = head;
    Node fastPtr = head;
    Node preSlow = head;

    if (head != null) 
    {
        while (fastPtr != null && fastPtr.next != null) 
        {

            fastPtr = fastPtr.next.next;
            preSlow = slowPtr;
            slowPtr = slowPtr.next;
        }

        if (fastPtr != null)
        {
            return slowPtr.value;
        }
        else
        {
            return (slowPtr.value + preSlow.value) / 2;
        }
    }
    return 0; 
}
```
