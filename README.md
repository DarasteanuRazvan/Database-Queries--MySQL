# Database-Queries--MySQL

1. 
SELECT * FROM User;

SELECT firstName, lastName FROM User;

SELECT email FROM User WHERE id = 1;

SELECT * FROM User WHERE country = 'United States';

SELECT * FROM User WHERE gender = 'Male' AND city = 'Iasi';

SELECT firstName, lastName, nationality FROM User WHERE dateOfBirth BETWEEN '1990-01-01' AND '1999-12-31';

SELECT id, email FROM User ORDER BY email ASC;

SELECT firstName, lastName, country FROM User ORDER BY lastName DESC LIMIT 10;

SELECT id, email FROM User WHERE email LIKE '%@gmail.com%';

2. 
SELECT * FROM Room;

SELECT description, price, hotelId, id FROM Room WHERE maximumNumberOfGuests >= 3;

SELECT description, price FROM Room;

SELECT * FROM Room WHERE breakfastIncluded = TRUE;

SELECT type, COUNT(*) AS num_rooms FROM Room GROUP BY type;

SELECT * FROM Room WHERE price = (SELECT MAX(price) FROM Room);

SELECT AVG(price) as avg_price FROM Room;

SELECT * FROM Room WHERE maximumNumberOfGuests >= 4;

3.
SELECT * FROM Hotel;

SELECT id, name FROM Hotel;

SELECT name, starRating, userRating, location FROM Hotel;

SELECT name, description, amenities, pricePerBreakfast FROM Hotel;

SELECT id, name, breakfastAsOption FROM Hotel WHERE breakfastAsOption = TRUE;

SELECT * FROM Hotel WHERE id = '4a47d1ea-ce18-4239-bdd8-a9eecfb1b26a';
4.
INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('87506b5a-3df8-4967-9379-265925aa9873', 'Example Hotel', 'This is an example hotel description.', '4', '9', 'Pool, Gym, Free Wi-Fi', '11', '1', '1', 'Pascani');

INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('77506b5a-3df8-4967-9379-265925aa9873', 'The Grand Hotel', 'Experience luxury at its finest.', '5', '9', 'Spa, Restaurant, Free Parking', '19', '0', '1', 'Suceava');

INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('67506b5a-3df8-4967-9379-265925aa9873', 'The Beach Resort', 'Enjoy the beautiful views of the ocean.', '3', '8', 'Beach Access, Bar, Free Breakfast', '6', '1', '0', 'Vaslui');

INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('17506b5a-3df8-4967-9379-265925aa9873', 'Grand Hotel', 'Luxury hotel in the heart of the city', '5', '5', 'Pool, Spa, Gym, Restaurant', '16', '1', '1', 'Bacau');

INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('3f3c1d34-542a-40f2-81c2-2ed9d553d208', 'The Ritz', 'Iconic hotel in downtown', '5', '4.5', 'Spa, Fitness center, Rooftop bar, Fine dining', '25', '0', '1', 'Piatra Neamt');

INSERT INTO Hotel (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('f3c52856-4d4b-4cb4-92ee-4d615e5e5a38', 'Hilton Garden Inn', 'Modern hotel in business district', '4', '4.2', 'Fitness center, Meeting rooms, 24-hour convenience store', '10', '1', '0', 'Botosani');

DELETE FROM Hotel WHERE id = '87506b5a-3df8-4967-9379-265925aa9873';

DELETE FROM Hotel WHERE id = '77506b5a-3df8-4967-9379-265925aa9873';

DELETE FROM Hotel WHERE id = '67506b5a-3df8-4967-9379-265925aa9873';

DELETE FROM Hotel WHERE id = '17506b5a-3df8-4967-9379-265925aa9873';

DELETE FROM Hotel WHERE id = '3f3c1d34-542a-40f2-81c2-2ed9d553d208';

DELETE FROM Hotel WHERE id = 'f3c52856-4d4b-4cb4-92ee-4d615e5e5a38';


5.
INSERT INTO _history (A, B, id)
VALUES ('87506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 178);

INSERT INTO _history (A, B, id)
VALUES ('77506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 179);

INSERT INTO _history (A, B, id)
VALUES ('67506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 180);

INSERT INTO _history (A, B, id)
VALUES ('17506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 181);

INSERT INTO _history (A, B, id)
VALUES ('3f3c1d34-542a-40f2-81c2-2ed9d553d208', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 182);

INSERT INTO _history (A, B, id)
VALUES ('f3c52856-4d4b-4cb4-92ee-4d615e5e5a38', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 183);

DELETE FROM _history WHERE A = '87506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 178;

DELETE FROM _history WHERE A = '77506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 179;

DELETE FROM _history WHERE A = '67506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 180;

DELETE FROM _history WHERE A = '17506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 181;

DELETE FROM _history WHERE A = '3f3c1d34-542a-40f2-81c2-2ed9d553d208' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 182;

DELETE FROM _history WHERE A = 'f3c52856-4d4b-4cb4-92ee-4d615e5e5a38' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 183;
6.
INSERT INTO _favorites (A, B, id)
VALUES ('87506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 178);

INSERT INTO _favorites (A, B, id)
VALUES ('77506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 179);

INSERT INTO _favorites (A, B, id)
VALUES ('67506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 180);

INSERT INTO _favorites (A, B, id)
VALUES ('17506b5a-3df8-4967-9379-265925aa9873', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 181);

INSERT INTO _favorites (A, B, id)
VALUES ('3f3c1d34-542a-40f2-81c2-2ed9d553d208', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 182);

INSERT INTO _favorites (A, B, id)
VALUES ('f3c52856-4d4b-4cb4-92ee-4d615e5e5a38', '1b69bcf9-5512-4cc0-aa27-02ed09ec274a', 183);

DELETE FROM _favorites WHERE A = '87506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 178;

DELETE FROM _favorites WHERE A = '77506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 179;

DELETE FROM _favorites WHERE A = '67506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 180;

DELETE FROM _favorites WHERE A = '17506b5a-3df8-4967-9379-265925aa9873' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 181;

DELETE FROM _favorites WHERE A = '3f3c1d34-542a-40f2-81c2-2ed9d553d208' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 182;

DELETE FROM _favorites WHERE A = 'f3c52856-4d4b-4cb4-92ee-4d615e5e5a38' AND B ='1b69bcf9-5512-4cc0-aa27-02ed09ec274a' AND id = 183;

7.
UPDATE Room SET price = 180 WHERE id = 178;

UPDATE Room SET description = 'Spacious room with a view of the ocean', img = 'ocean_view.jpg' WHERE id = 179;

UPDATE Room SET type = 'triple' WHERE id = 180;

UPDATE Room SET maximumNumberOfGuests = maximumNumberOfGuests + 2 WHERE id = 181;

UPDATE Room SET breakfastIncluded = 'FALSE' WHERE hotelId = '67506b5a-3df8-4967-9379-265925aa9873';

UPDATE Room SET type = 'Camera copiilor' WHERE id = 182;

SELECT * FROM Room;
8.
SELECT * FROM TimeInterval;

INSERT INTO TimeInterval (id, min, max, hotelId)
VALUES (111, '2023-04-12', '2023-04-16', '97506b5a-3df8-4967-9379-265925aa9873');

UPDATE TimeInterval SET `min` = '2025-01-03', `max` = '2025-02-03' WHERE id = 'b9d6a4bb-6a6b-49d6-9b10-617d362c1da4' AND hotelId = '4a47d1ea-ce18-4239-bdd8-a9eecfb1b26a';

DELETE FROM TimeInterval
WHERE id = 111 AND `min` = '2023-04-12' AND `max` = '2023-04-16' AND hotelId = '97506b5a-3df8-4967-9379-265925aa9873';

9.
ALTER TABLE Hotel ADD COLUMN bookedRooms INT DEFAULT 0;

ALTER TABLE Hotel DROP COLUMN bookedRooms;

SELECT * FROM Hotel;

10. 
CREATE TABLE Hotel_Sovata (
  id VARCHAR(36) PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  description TEXT,
  starRating INT,
  userRating FLOAT,
  amenities VARCHAR(255),
  pricePerBreakfast DECIMAL(10,2),
  allowsPets BOOLEAN,
  breakfastAsOption BOOLEAN,
  location VARCHAR(255)
);

INSERT INTO Hotel_Sovata (id, name, description, starRating, userRating, amenities, pricePerBreakfast, allowsPets, breakfastAsOption, location)
VALUES ('87506b51-3df8-4967-9379-265925aa9873', 'Hotel Sovata', 'This is a beautiful hotel.', '4', '9', 'Pool, Gym, Free Wi-Fi', '11', '1', '1', 'Sovata');

SELECT * FROM Hotel_Sovata;

DROP TABLE Hotel_Sovata;

