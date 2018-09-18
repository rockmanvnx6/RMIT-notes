# Heuristics, Design Priciples and Design laws

## Nielson's 10 Heuristic

1. Visibility of system status
   - The system should always keep users informed what is going on in the background.

2. Match between system and the real world
   - The system should speak the user's language, phases and concepts should be user familiar than system-oriented terms.
   - **Example:** `404 notfound` should be replaced with `The page you're looking for is not found`

3. User control and freedom
   - Users often make mistakes when using the system. The system should have emergency exit, something like undo or go back so the users can control.

4. Consistency and standard

   - Use the same words for the same thing
   - **Example:** choosing either `exit`, `log out` or `leave`

   - Remain the same navigation UI model.

5. Error prevention

   - User friendly error messages are good but it's better to prevent the error before users even make it. 
   - One way is to make a confirmation button so users have to commit to the action

6. Recognition rather than recall

   - User should not have to memorise the functions of the app.
   - Use layouts, graphic design so the user can interact with the graphic easily.

7. Flexibility and Efficiency of use

   - Allow expert users to use shortcuts
   - Scaling functionality depending on user's skills.

8. Aesthetic and minimalist design

   - Dialogues should not contain information which is irrelevant or rarely needed.
   - Try to make things simple

9. Recognize, diagnose and recover

   - Error messages should be clear and natural, precise, not intimidate or blame the user
   - Good error messages help user to solve thier problem, learn more about the system
   - **Example:** Google: "did you mean to search ..."

10. Help and documentation

    - It's better to make the user get used to the system but however help and documentation is still neccessary
    - The document has to contain the information that users need and don't contain any extra information.

## Design principle

- Heuristics are commonly applied on an existing system or prototype.
- Design principles are used to analyse the system interface and information architecture.
- These are **guidelines, not rules**



> ### Principle of proximity
>
> - Buttons that in the same group of function should be together.
> - **Example:** "Yes" would be highly expected to next to "No"
>
> #### Visibility and visual feedback
>
> - Promince
>   - Putting the more important items larger than the less important one. So users will focus on the important items first.
> - Opacity
>   - Chagne the opacity to bring items into focus
> - Typeface
>   - The font must be clear to increase readability 
> - Colour and contrast
>   - Higher contrast or brighter colours will draw more attention

>### Affordance
>
>- Make things easier to do intuitively
>- Make things harder to do it wrong
>- **Example: ** The three prong electrical plug is harder to do it wrong.

> ### Status
>
> - Always indicate the background task or system status to the user. Either it's processing or wating for user's input
> - Like Heuristic 1 - Visibility of system status

> ### Consistency
>
> - Keep everything consistent in terms of interaction placement, colours and type of interface.
> - Do not keep switching your navigation bar.

## Design Laws

> - **Hicks law:**
>   - The more choices, the more complicated
> - **Fitt's law**
>   - It's faster to hit larger target which closer to you than smaller targets further than you.