*** Settings ***
Library  SeleniumLibrary

*** Variables ***
${browser}  chrome
${url}  https://www.saucedemo.com

*** Test Cases ***
LoginTest
    Given Login
    And Adding to cart
    Then Enter credentials
    Then Verify and finish



*** Keywords ***
Login
    open browser  ${url}  ${browser}
    input text  xpath://*[@id="user-name"]  standard_user
    input text  xpath://input[@id='password']  secret_sauce
    click element  xpath://*[@id="login-button"]

Adding to cart
    click element  xpath://*[@id="inventory_container"]/div/div[1]/div[3]/button
    click element  xpath://*[@id="shopping_cart_container"]/a/span
    click element  xpath://*[@id="cart_contents_container"]/div/div[2]/a[2]

Enter credentials
    input text  xpath://*[@id="first-name"]  Chethan
    input text  xpath://*[@id="last-name"]  Sanjay
    input text  xpath://*[@id="postal-code"]  560041

Verify and finish
    click element  xpath://*[@id="checkout_info_container"]/div/form/div[2]/input
    click element  xpath://*[@id="checkout_summary_container"]/div/div[2]/div[8]/a[2]
