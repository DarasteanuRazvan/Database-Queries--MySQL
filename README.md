# Database-Queries--MySQL Project

Welcome to the Database-Queries--MySQL project repository! 🚀 This repository showcases various MySQL queries designed for the management of a hotel-related database. Below is a summary of the key queries and operations performed:

## User Queries

1. **Retrieve All Users:**
   ```sql
   SELECT * FROM User;
   ```

2. **Retrieve Specific User Attributes:**
   ```sql
   SELECT firstName, lastName FROM User;
   ```

3. **Retrieve User by ID:**
   ```sql
   SELECT email FROM User WHERE id = 1;
   ```

4. **Filter Users by Country:**
   ```sql
   SELECT * FROM User WHERE country = 'United States';
   ```

5. **Complex User Filtering:**
   ```sql
   SELECT * FROM User WHERE gender = 'Male' AND city = 'Iasi';
   ```

6. **User Filtering by Date of Birth Range:**
   ```sql
   SELECT firstName, lastName, nationality FROM User WHERE dateOfBirth BETWEEN '1990-01-01' AND '1999-12-31';
   ```

7. **Order Users by Email:**
   ```sql
   SELECT id, email FROM User ORDER BY email ASC;
   ```

8. **Top 10 Users Ordered by Last Name:**
   ```sql
   SELECT firstName, lastName, country FROM User ORDER BY lastName DESC LIMIT 10;
   ```

9. **Filter Users by Email Domain:**
   ```sql
   SELECT id, email FROM User WHERE email LIKE '%@gmail.com%';
   ```

## Room and Hotel Queries

10. **Retrieve All Rooms:**
    ```sql
    SELECT * FROM Room;
    ```

11. **Retrieve Specific Room Attributes:**
    ```sql
    SELECT description, price, hotelId, id FROM Room WHERE maximumNumberOfGuests >= 3;
    ```

12. **Retrieve Room Descriptions and Prices:**
    ```sql
    SELECT description, price FROM Room;
    ```

13. **Filter Rooms with Breakfast Included:**
    ```sql
    SELECT * FROM Room WHERE breakfastIncluded = TRUE;
    ```

14. **Count Rooms Grouped by Type:**
    ```sql
    SELECT type, COUNT(*) AS num_rooms FROM Room GROUP BY type;
    ```

15. **Retrieve Room with Maximum Price:**
    ```sql
    SELECT * FROM Room WHERE price = (SELECT MAX(price) FROM Room);
    ```

16. **Calculate Average Room Price:**
    ```sql
    SELECT AVG(price) as avg_price FROM Room;
    ```

17. **Filter Rooms by Maximum Number of Guests:**
    ```sql
    SELECT * FROM Room WHERE maximumNumberOfGuests >= 4;
    ```

## Hotel Management Queries

18. **Retrieve All Hotels:**
    ```sql
    SELECT * FROM Hotel;
    ```

19. **Retrieve Hotel IDs and Names:**
    ```sql
    SELECT id, name FROM Hotel;
    ```

20. **Retrieve Hotel Details:**
    ```sql
    SELECT name, starRating, userRating, location FROM Hotel;
    ```

21. **Retrieve Hotel Amenities and Pricing:**
    ```sql
    SELECT name, description, amenities, pricePerBreakfast FROM Hotel;
    ```

22. **Retrieve Hotels Offering Breakfast:**
    ```sql
    SELECT id, name, breakfastAsOption FROM Hotel WHERE breakfastAsOption = TRUE;
    ```

23. **Insert New Hotel:**
    ```sql
    INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location) VALUES ('87506b5a-3df8-4967-9379-265925aa9873', 'Example Hotel', 'This is an example hotel description.', '4', '9', 'Pool, Gym, Free Wi-Fi', '11', '1', '1', 'Pascani');
    ```

24. **Delete Hotels by ID:**
    ```sql
    DELETE FROM Hotel WHERE id IN ('87506b5a-3df8-4967-9379-265925aa9873', '77506b5a-3df8-4967-9379-265925aa9873', '67506b5a-3df8-4967-9379-265925aa9873', '17506b5a-3df8-4967-9379-265925aa9873', '3f3c1d34-542a-40f2-81c2-2ed9d553d208', 'f3c52856-4d4b-4cb4-92ee-4d615e5e5a38');
    ```

25. **Hotel History and Favorites Operations:**
    - Insert, Delete, and Update operations on the `_history` and `_favorites` tables.

26. **Update Room Attributes:**
    ```sql
    UPDATE Room SET price = 180 WHERE id = 178;
    ```

27. **Update Room Description and Image:**
    ```sql
    UPDATE Room SET description = 'Spacious room with a view of the ocean', img = 'ocean_view.jpg' WHERE id = 179;
    ```

28. **Update Room Type:**
    ```sql
    UPDATE Room SET type = 'triple' WHERE id = 180;
    ``

`

29. **Increase Maximum Guests for a Room:**
    ```sql
    UPDATE Room SET maximumNumberOfGuests = maximumNumberOfGuests + 2 WHERE id = 181;
    ```

30. **Disable Breakfast for Rooms in a Specific Hotel:**
    ```sql
    UPDATE Room SET breakfastIncluded = 'FALSE' WHERE hotelId = '67506b5a-3df8-4967-9379-265925aa9873';
    ```

31. **Update Room Type:**
    ```sql
    UPDATE Room SET type = 'Camera copiilor' WHERE id = 182;
    ```

32. **Retrieve Updated Room Data:**
    ```sql
    SELECT * FROM Room;
    ```

33. **Time Interval Operations:**
    - Insert, Update, and Delete operations on the `TimeInterval` table.

34. **Hotel Schema Modification:**
    - Adding and dropping columns to the `Hotel` table.

35. **Create and Drop a New Hotel Table:**
    - Create a new `Hotel_Sovata` table and then drop it.

Feel free to explore and experiment with these queries! If you have any questions or suggestions, don't hesitate to reach out. Happy querying! 🛌🏨
