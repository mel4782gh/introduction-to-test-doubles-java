# Activity 5

## Test Doubles - Spy

### 🔎 Exercise 5.1 - Recap - What is a Spy?

Firstly, let's remind ourselves what a Spy is.

- Can you remember what a Spy means?
we
<details>
<summary>Click here to see the answer</summary>
<pre>

Spies enable you to focus (spy on) specific methods on a real object. We call this object the ‘spied object’.

</pre>
</details>

---

### 🔎 Exercise 5.2 - Let's see the Spy in action!

- Head over to the [BubbleTeaOrderServiceSpyTest.java](../src/test/java/BubbleTeaOrderServiceSpyTest.java) file.


- Which line of code creates the Spy on the `BubbleTeaMessenger`?

<details>
<summary>Click here to see the answer</summary>
<pre>

// Line 25
spiedMessenger = spy(new BubbleTeaMessenger(dummySimpleLogger));

</pre>
</details>


- This differs from the Mock object because it is our actual `BubbleTeaMessenger` in action here and it
has been infiltrated! 😬
  
- We can verify the calls made to our real `BubbleTeaMessenger`, for example:

```

//Check the spied messenger was called with BubbleTeaOrderRequest result
verify(spiedMessenger).sendBubbleTeaOrderRequestEmail(result);
verify(spiedMessenger, times(1)).sendBubbleTeaOrderRequestEmail(result);

```

- Does it look familiar? You saw this before in [Activity_3](activity_3.md) for Mocks.
  

- The key difference here is with a Spy, you are peering into the real object, real methods and verifying calls to it.

---

### 🥳 Congratulations!

You have now completed the activities!

Feel free to head back to review the concepts again.
We encourage you to do some of your own research and experimentation in your own time to explore these concepts further.

### Extension

- Can you find a way to test multiple different Bubble Tea Requests without having to repeat the same test code again
and again? **Hint**: You may want to have a think about test parameterisation.
  
---
### Key Study Notes

☑️ A Spy enables you to focus (spy on) specific methods on a real object. We call this object the ‘spied object’.
