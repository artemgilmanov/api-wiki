**PUT Verb**
- Used to modify resource(s)
- Should contain a message body that specifies the resource to be modified
- Should not contain query string parameters
- What happens if the resource to modify does not exist?
  - The spec states a new resource should be created. PUT should behave as POST.
  - Use your own discretion
- PUT is idempotent. A property of an action that can be applied many times, and the result will always be the same.
