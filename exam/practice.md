# Practice Exam INT305

## Write a XML Schema Definition (XSD) file of the following XML document (without namespace)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<FoodChain>
    <Company id="1">
        <Name>BurgerTown</Name>
        <Headquarters>New York, USA</Headquarters>
        <EstablishedYear>1985</EstablishedYear>
        <Branches>
            <Branch id="101">
                <Location>Los Angeles, USA</Location>
                <Employees>120</Employees>
                <Manager>
                    <Name>John Doe</Name>
                    <Contact>
                        <Email>john.doe@burgertown.com</Email>
                        <Phone>+1-213-456-7890</Phone>
                    </Contact>
                </Manager>
                <Menu>
                    <Item id="M101">
                        <Name>Classic Burger</Name>
                        <Category>Burger</Category>
                        <Price currency="USD">7.99</Price>
                    </Item>
                    <Item id="M102">
                        <Name>Cheeseburger</Name>
                        <Category>Burger</Category>
                        <Price currency="USD">8.49</Price>
                    </Item>
                    <Item id="M103">
                        <Name>French Fries</Name>
                        <Category>Side</Category>
                        <Price currency="USD">2.99</Price>
                    </Item>
                </Menu>
            </Branch>
            <Branch id="102">
                <Location>Chicago, USA</Location>
                <Employees>95</Employees>
                <Manager>
                    <Name>Jane Smith</Name>
                    <Contact>
                        <Email>jane.smith@burgertown.com</Email>
                        <Phone>+1-312-987-6543</Phone>
                    </Contact>
                </Manager>
                <Menu>
                    <Item id="M104">
                        <Name>Veggie Burger</Name>
                        <Category>Burger</Category>
                        <Price currency="USD">7.49</Price>
                    </Item>
                    <Item id="M105">
                        <Name>Onion Rings</Name>
                        <Category>Side</Category>
                        <Price currency="USD">3.49</Price>
                    </Item>
                </Menu>
            </Branch>
        </Branches>
    </Company>

    <Company id="2">
        <Name>PastaParadise</Name>
        <Headquarters>Rome, Italy</Headquarters>
        <EstablishedYear>1995</EstablishedYear>
        <Branches>
            <Branch id="201">
                <Location>Florence, Italy</Location>
                <Employees>60</Employees>
                <Manager>
                    <Name>Marco Rossi</Name>
                    <Contact>
                        <Email>marco.rossi@pastaparadise.it</Email>
                        <Phone>+39-055-2233445</Phone>
                    </Contact>
                </Manager>
                <Menu>
                    <Item id="P101">
                        <Name>Spaghetti Carbonara</Name>
                        <Category>Pasta</Category>
                        <Price currency="EUR">12.50</Price>
                    </Item>
                    <Item id="P102">
                        <Name>Lasagna</Name>
                        <Category>Pasta</Category>
                        <Price currency="EUR">13.00</Price>
                    </Item>
                </Menu>
            </Branch>
            <Branch id="202">
                <Location>Milan, Italy</Location>
                <Employees>80</Employees>
                <Manager>
                    <Name>Giulia Bianchi</Name>
                    <Contact>
                        <Email>giulia.bianchi@pastaparadise.it</Email>
                        <Phone>+39-02-778899</Phone>
                    </Contact>
                </Manager>
                <Menu>
                    <Item id="P103">
                        <Name>Penne Arrabbiata</Name>
                        <Category>Pasta</Category>
                        <Price currency="EUR">11.00</Price>
                    </Item>
                    <Item id="P104">
                        <Name>Garlic Bread</Name>
                        <Category>Side</Category>
                        <Price currency="EUR">4.50</Price>
                    </Item>
                </Menu>
            </Branch>
        </Branches>
    </Company>
</FoodChain>
```

### Overview of the XML Structure

- Root Element: `<FoodChain>`
- Company Element: Each company in the food chain industry is represented by a `<Company>` element, with attributes such as id and child elements like Name, Headquarters, EstablishedYear, and nested elements like Branches.
- Branch Element: Each company has one or more `<Branch>` elements representing their locations, along with Location, Employees, and Manager (which includes Name and Contact details).
- Menu and Item Elements: Each branch has a menu represented by the `<Menu>` element, containing multiple `<Item>` elements. Each item includes Name, Category, Price, and an id attribute.

## Problems for Practicing XPath Queries:

You can query the XML data using XPath. Below are some problems that will help you explore various XPath topics comprehensively:

- **Select all company names in the food chain**:

  - "BurgerTown"
  - "PastaParadise"

- **Select the headquarters of the company named "BurgerTown"**:
  - "New York, USA"

- **Find all branches that have more than 100 employees**:

  - Branch id="101" (Location: Los Angeles, USA)

- **List all items in the menu where the price is greater than 10 USD or EUR**:
  - Spaghetti Carbonara (12.50 EUR)
  - Lasagna (13.00 EUR)
  - Penne Arrabbiata (11.00 EUR)

- **Select all branches with a specific `id` (e.g., branch with `id="101"`)**:

  - Branch id="101" (Location: Los Angeles, USA)

- **Retrieve the names of all food items that belong to the "Side" category**:
  - French Fries
  - Onion Rings
  - Garlic Bread

- **Select the email address of the manager of the branch located in Los Angeles**:

  - <john.doe@burgertown.com>

- **Get the names of all items served at the Florence branch**:
  - Spaghetti Carbonara
  - Lasagna

- **Calculate the total number of branches across all companies**:

  - 4 branches

- **Count how many menu items each branch offers**:
  - Los Angeles branch: 3 items
  - Chicago branch: 2 items
  - Florence branch: 2 items
  - Milan branch: 2 items

- **Select the names of items that have the same parent as the "Classic Burger" (i.e., its sibling items)**:

  - Cheeseburger
  - French Fries

- **Find all managers who are responsible for branches with more than 80 employees**:
  - John Doe (Los Angeles)
  - Jane Smith (Chicago)

- **Select all managers whose branches have more than 50 employees and serve a pasta dish**:

  - Marco Rossi (Florence)
  - Giulia Bianchi (Milan)

- **Find all menu items that are burgers and cost more than 8 USD**:
  - Cheeseburger (8.49 USD)

- **Select all elements that have the `Price` element as a child**:

  - Classic Burger
  - Cheeseburger
  - French Fries
  - Veggie Burger
  - Onion Rings
  - Spaghetti Carbonara
  - Lasagna
  - Penne Arrabbiata
  - Garlic Bread

- **Select all elements regardless of their tag names under the `<FoodChain>` root**:
  - Company elements and all their descendants, including BurgerTown and PastaParadise and their branches, managers, and menus.

- **Retrieve the menu item names with a price in "USD"**:

  - Classic Burger
  - Cheeseburger
  - French Fries
  - Veggie Burger
  - Onion Rings

- **Select all branches managed by people with the first name "Jane"**:
  - Branch id="102" (Location: Chicago, USA, Manager: Jane Smith)

- **Get the list of company names that have branches offering items in the "Pasta" category**:

  - PastaParadise

- **Select all food items served at branches located in Italy**:
  - Spaghetti Carbonara
  - Lasagna
  - Penne Arrabbiata
  - Garlic Bread
