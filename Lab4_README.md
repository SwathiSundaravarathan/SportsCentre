Swathi Sundaravarathan LAB 4 ReadmeFile

---Business Domain - Sports Centre---

    I have chosen this domain because it is one of the most popular field and business in almost 
every country across the world. One of the main reasons is that I am a sports person and I am 
highly motivated to work in this domain.

----Write a second paragraph answering the following questions: There is only one
entity required for Lab 4, but what other entities from your business domain can
you think of? How might they relate to one another? You can answer this in
narrative form, or you can answer it with a database diagram. One of your
midterm questions will be very similar, about the design of your FP, so this is to
help get you started early-----

![image](https://user-images.githubusercontent.com/97709529/153996566-e6b270d8-daa3-4929-9d4b-ad38473fc145.png)

The Entity which I have choosen is a Sports equipments. We can have practice centres for various game and can also conduct events 
for various age categories.

**Test Cases:**
**Test1**
#Create
public void create(){
    Sports test = new Sports("Test create", "Test Game", LocalDate.of(2020, 6, 6), SportType.VolleyBall); 
        tx.begin();
        em.persist(test);
        tx.commit();
        Sports findNewSport
               = em.createQuery("select s from Sports s where s.equipmentName = 'Test Equipment'", Sports.class).getSingleResult();   
         LOG.info(findNewSport.toString());
        assertNotNull(findNewSport);
        assertTrue(findNewSport.getId()>0);
        tx.begin();
        em.remove(test);
        tx.commit();
 //In this block we are creating a new row and checking if its available  
 ----------------------------------------------------------------------------------------------------
** Test2**
 #Read
 public void read(){
        Sports test
                = em.createQuery("select s from Sports s where s.equipmentName = 'Test Equipment'", Sports.class).getSingleResult();

        assertNotNull(test);
        assertEquals("Test Equipment", test.getEquipmentName());
    }
    
//In this block we are using select query to find the given value from the table
-----------------------------------------------------------------------------------------------------
**Test3**
#Update
public void update(){
        Sports test
                = em.createQuery("select s from Sports s where s.equipmentName = 'Test Equipment'", Sports.class).getSingleResult();

        tx.begin();
        test.setType(SportType.Hockey);
        tx.commit();
        Sports readBackFromDatabaseToVerifyChange
                = em.createQuery("select s from Sports s where s.equipmentName = 'Test Equipment'", Sports.class).getSingleResult();

        LOG.info("update test case: " + readBackFromDatabaseToVerifyChange.toString());
        
        assertEquals(SportType.Hockey, readBackFromDatabaseToVerifyChange.getType());
    }
//In this block we are updating a row in the table and checking if it gets updated in the database
----------------------------------------------------------------------------------------------------
**Test4**
#Delete
public void delete(){
        Sports test = new Sports("Test Delete", "Test Game", LocalDate.of(2020, 6, 6), SportType.Badminton);
        tx.begin();
        em.persist(test);
        tx.commit();
        assertNotNull(test.getId());
        LOG.info("test delete: " + test.toString());

        tx.begin();
        em.remove(test);
        tx.commit();
        
        LOG.info("test delete: " + test.toString());
        Sports checkIfSportDeleted = em.find(Sports.class, test.getId());
        assertNull(checkIfSportDeleted);
        
//In this block we are creating a new row and deleting it.
-----------------------------------------------------------------------------------------------
**Test5**
public void testInvalidEquipmentNameValidationShouldFail() {
        Sports sport = new Sports("", "Test Game1", LocalDate.of(2020, 6, 6), SportType.Hockey);
        Set<ConstraintViolation<Sports>> violations = validator.validate(sport);
        for (ConstraintViolation<Sports> violation : violations) {
            System.out.println(violation.toString());
        }
        assertEquals(1, violations.size());
        assertEquals("must not be blank", violations.iterator().next().getMessage());
        
    }
  
//In this block we are passing empty name in the column EquipmentName and checking for violation
  -----------------------------------------------------------------------------------------------
**  Test6**
  public void validEquipmentNameValidationShouldPass() {
        Sports sport = new Sports("Test Equipment1", "Test Game1", LocalDate.of(2020, 6, 6), SportType.Hockey);
        Set<ConstraintViolation<Sports>> violations = validator.validate(sport);
        for (ConstraintViolation<Sports> violation : violations) {
            System.out.println(violation.toString());
        }
        assertEquals(0, violations.size());
    }
  
  //In this block we are passing the correct value and checking for violation
  ----------------------------------------------------------------------------------------------------
  **Test7**
  public void testInvalidGameNameValidationShouldFail() {
        Sports sport = new Sports("Test Equipment2", "", LocalDate.of(2020, 6, 6), SportType.Hockey);
        Set<ConstraintViolation<Sports>> violations = validator.validate(sport);
        for (ConstraintViolation<Sports> violation : violations) {
            System.out.println(violation.toString());
        }
        assertEquals(2, violations.size());        
    }
  ///Empty GameName value is passed( this Violates both conditions 
    that not blank and also it is mismatching with the size.
  ------------------------------------------------------------------------------------------------------
**  Test8**
  public void validGameNameValidationShouldPass() {
        Sports sport = new Sports("Test Equipment2", "Test Game2", LocalDate.of(2020, 6, 6), SportType.Hockey);
        Set<ConstraintViolation<Sports>> violations = validator.validate(sport);
        for (ConstraintViolation<Sports> violation : violations) {
            System.out.println(violation.toString());
        }
        assertEquals(0, violations.size());
    }
  //Correct Values are passed
  ----------------------------------------------------------------------------------------------------------
  **Test9**
  public void testInvalidManufacturingDateValidationShouldFail() {
        Sports sport = new Sports("Test Equipment3", "Test Game3", LocalDate.of(2024, 6, 6), SportType.Hockey);
        Set<ConstraintViolation<Sports>> violations = validator.validate(sport);
        for (ConstraintViolation<Sports> violation : violations) {
            System.out.println(violation.toString());
        }
        assertEquals(1, violations.size());        
    }
  //Future date is passed in manufacturingDate column
  ---------------------------------------------------------------------------------------------------------------
 ***Test10***
  public void validManufacturingDateValidationShouldPass() {
        Sports sport = new Sports("Test Equipment3", "Test Game3", LocalDate.of(2020, 6, 6), SportType.Hockey);
        Set<ConstraintViolation<Sports>> violations = validator.validate(sport);
        for (ConstraintViolation<Sports> violation : violations) {
            System.out.println(violation.toString());
        }
        assertEquals(0, violations.size());
    }
  //Past or present date is passed
  -------------------------------------------------------------------------------------------------------------------
    
OutPut Screenshot for Test Cases

![image](https://user-images.githubusercontent.com/97709529/153996895-9585b871-1cfb-481d-80ad-69ab8567c2cf.png)
  
  
