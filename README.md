# Health-Graph-QA-Automation
POM CLASS FOR THE ASSIGNMENT
package pomClasses;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.FindBy;
import org.openqa.selenium.support.PageFactory;
import org.openqa.selenium.support.ui.Select;

public class HeltCare {
	//Locator For LoginUser
		@FindBy(xpath="//font[text()='Sign In']")private WebElement Signinbtn;
		@FindBy(xpath="//input[@id=\"uid\"]")private WebElement Uid;
		@FindBy(xpath="//input[@id=\"passw\"]")private WebElement Pass;
		@FindBy(xpath="//input[@name=\"btnSubmit\"]")private WebElement Loginbtn;
	//Locator For Admin Login Account Summary Details 
		@FindBy(xpath="/html/body/table[2]/tbody/tr/td[2]/div/p")private WebElement Admin;
		@FindBy(xpath="//a[text()='View Account Summary']")private WebElement AccSummery;
		@FindBy(xpath="//select[@id=\"listAccounts\"]")private WebElement SelectAcc;
		@FindBy(xpath="//input[@id='btnGetAccount']")private WebElement Gobtn;
		@FindBy(xpath="/html/body/table[2]/tbody/tr/td[2]/div/table/tbody/tr[1]/td/table/tbody/tr[4]/td[2]")private WebElement Balvalidate; ;
	//Locator for Transfer Funds 	
		@FindBy(xpath="//a[text()='Transfer Funds']")private WebElement Trfunds ;
		@FindBy(xpath="//select[@id=\'toAccount\']")private WebElement Trtoacc ;
		@FindBy(xpath="//input[@id='transferAmount']")private WebElement Amttoacc ;
		@FindBy(xpath="//input[@id='transfer']")private WebElement Trmoneybtn;
		@FindBy(xpath="//*[@id=\"ctl0_ctl0_Content_Main_postResp\"]/span")private WebElement TRfundSucc ;
		@FindBy(xpath="//a[@id=\"MenuHyperLink2\"]")private WebElement ViewTr ;
		@FindBy(xpath="(//td[text()='$9876.00'])[1]")private WebElement FristTrvalid ;
	//Locator for Contact US Btn
		@FindBy(xpath="//a[text()='Contact Us']")private WebElement ContUs ;
		@FindBy(xpath="//a[text()='online form']")private WebElement onlinebtn ;
	//Locator for Online Form Details
		@FindBy(xpath="//input[@name='email_addr']")private WebElement OnlineEmail ;
		@FindBy(xpath="//input[@name='subject']")private WebElement OnlineSubject ;
		@FindBy(xpath="//textarea[@name=\"comments\"]")private WebElement OnlineComments;
		@FindBy(xpath="(//input[@type='submit'])[2]")private WebElement OnlineSubmit ;
	//Locator for SignOFF
		@FindBy(xpath="//font[text()='Sign Off']")private WebElement SignOff ;
	
	//Iitializatin Using Constructor
		public HeltCare(WebDriver driver){
			PageFactory.initElements(driver, this);
		}
		
	//Usage In Methods
		public void clickSigninbtn() 
		{
			Signinbtn.click();
		}
		public String EnterUserid(String uid) 
		{
			Uid.sendKeys(uid);
			return uid;
		}
		public String EnterPass(String pid) 
		{
			Pass.sendKeys(pid);
			return pid;
		}
		
		public void clickloginbtn() 
		{
			Loginbtn.click();	
		}
		public String gettextadmin() {
			String actualadmin = Admin.getText();
			return actualadmin;
		}
		public void clickAccSummery() {
			AccSummery.click();
		}
		public void SelectAcc() {
			Select s = new Select(SelectAcc);
			s.selectByVisibleText("800001 Checking");	
		}
		public void clickGobtn() {
			Gobtn.click();
		}
		public String gettextBalvalidate() {
			String actualBal = Balvalidate.getText();
			return actualBal;
	    }
		public void clickTrfunds() {
			Trfunds.click();
		}
		public void selectTrtoacc() {
			Select s = new Select(Trtoacc);
			s.selectByVisibleText("800001 Checking");
		}
		public String enterAmttoacc(String Amt) {
			Amttoacc.sendKeys(Amt);
			return Amt;
		}
		public void clickTrmoney() {
			Trmoneybtn.click();
		}
		public String gettextTRfundSucc() {
			String actualTRfundSucc = TRfundSucc.getText();
			return actualTRfundSucc;
	    }
		public void clickViewTr() {
			ViewTr.click();
		}
		
		public String gettextFristTrvalid() {
			String actualFristTrvalid  = FristTrvalid.getText();
			return actualFristTrvalid ;
		}	
		
		public void clickContUs() {
			ContUs.click();
		}
		public void clickonlinebtn() {
			onlinebtn.click();
		}
		public String EnterOnlineEmail(String email) 
		{
			OnlineEmail.sendKeys(email);
			return email;
		}
		public String EnterOnlineSubject(String sub) 
		{
			OnlineSubject.sendKeys(sub);
			return sub;
		}
		public String EnterOnlineComments(String com) 
		{
			OnlineComments.sendKeys(com);
			return com;
		}
		public void clickOnlineSubmit() {
			OnlineSubmit.click();
		}
		public void clickSignOff() {
			SignOff.click();
		}
		
		
	}


