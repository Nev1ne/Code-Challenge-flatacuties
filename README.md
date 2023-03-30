# Code-Challenge-flatacuties
Today you'll be building an app for voting for the cutest animal! You will be
using a local API and building out the frontend for our app, Flatacuties.
## Demo

@@ -46,13 +46,13 @@ As a user, I can:
      "id": 1,
      "name": "Mr. Cute",
      "image": "https://thumbs.gfycat.com/EquatorialIckyCat-max-1mb.gif",
      "calories": 0
      "votes": 0
    },
    {
      "id": 2,
      "name": "Mr. Monkey",
      "image": "https://thumbs.gfycat.com/FatalInnocentAmericanshorthair-max-1mb.gif",
      "calories": 0
      "votes": 0
    },
    ...
   ]
@@ -71,10 +71,93 @@ As a user, I can:
    "id": 1,
    "name": "Mr. Cute",
    "image": "https://thumbs.gfycat.com/EquatorialIckyCat-max-1mb.gif",
    "calories": 0
    "votes": 0
   }
   ```

3. When the `form#calories-form` is submitted, add the number of calories from
3. When the `form#votes-form` is submitted, add the number of votes from
   the input field to the character displayed in the `div#detailed-info`. **No
   persistence is needed**.

### Bonus Deliverables

These bonus deliverables are here if you want an extra challenge and won't
affect your score. **Make sure to commit your work to save your progress before
attempting the bonus deliverables!**

In the `index.html` file, there is some additional HTML that is currently
commented out below the Reset Votes button. Remove the comments (delete the
`<!--` and `-->` code around the elements) so you can complete the bonus
deliverables.

1. When the Reset Votes button is clicked, reset the votes back to 0.

2. When the `form#character-form` is submitted, add a new character to the
   `div#character-bar`. The new character in the character bar should behave the
   same as the other characters when clicked (its details should be displayed
   below, and it should have functionality to add votes).

3. In addition to adding the character to the `div#character-bar` upon
   submitting the form, the character's details should show up immediately in
   the `div#detailed-info`.

### Extra Bonus

These extra bonus deliverables involve using `fetch` to update data on the
`json-server` backend by using `POST`, `PATCH`, and `DELETE` requests. These are
meant for an extra, extra challenge and won't affect your grade. **Make sure to
commit your work to save your progress before attempting the extra bonus
deliverables!**

1. When a user adds or resets the votes for a character, in addition to
   displaying the updated votes on the page, the votes should **also** be
   updated on the server. You will need to make a request that follows this
   structure:

    ```txt
    PATCH /characters/:id
    Request Headers: {
      Content-Type: application/json
    }
    Request Body: {
      "votes": 100
    }
    ----
    Example Response: {
      "id": 1,
      "name": "Mr. Cute",
      "image": "https://thumbs.gfycat.com/EquatorialIckyCat-max-1mb.gif",
      "votes": 100
    }
    ```

2. When a user adds a new character to the page using the character form, in
   addition to having the character show up on the page, it should **also** be
   saved to the server. You will need to make a request that follows this
   structure:

    ```txt
    POST /characters
    Request Headers: {
      Content-Type: application/json
    }
    Request Body: {
      "name": "Character Name",
      "image": "https://example.com/my-image.gif",
      "votes": 0
    }
    ----
    Example Response: {
      "id": 6,
      "name": "Character Name",
      "image": "https://example.com/my-image.gif",
      "votes": 0
    }
    ```
