# TEST-Project

package appModule;

import org.testng.Reporter;

import pageObject.AddEmployee_Page;
import pageObject.Left_Menu_Objects;
import pageObject.LogIn_Page;
import pageObject.BaseClass;
import utility.Constant1;
import utility.EmployeeData;
import utility.ExcelUtils;
import utility.Log;
import org.openqa.selenium.*;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import pageObject.AddEmployee_Page;

    public class EmployeeUpdate_Action extends BaseClass  {
    	
     
    	
			
		public EmployeeUpdate_Action(WebDriver driver) {
			super(driver);
			// TODO Auto-generated constructor stub
		}
		
		

		public static void Execute(int iTestCaseRow) throws Exception{
        	 
			
        Left_Menu_Objects.Menu_Employees().click();
        Log.info("Click Action performed on Employee menu");
        Thread.sleep(2000);
        
       
        String sClientName = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_ClientName);
        AddEmployee_Page.ClientName().sendKeys(sClientName);
        // Printing the logs for what we have just performed
        Log.info(sClientName+" is Select in client drop down");
        Thread.sleep(2000);
        
        
        driver.findElement(By.xpath("//html")).click();
        Log.info("Click action perform on blank screen");
        
        
        String sFilterFields = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_FullName );
	    AddEmployee_Page.txbx_FilterFields().sendKeys(sFilterFields);
	    // Printing the logs for what we have just performed
	    Log.info(sFilterFields+" is selected in relationship drop down text box" );
	    Thread.sleep(2000);
	    
	    
	    AddEmployee_Page.lnk_Edit().click();
		Log.info("Click action perform on Edit link");
		
		
		String sFullName = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_FullName);
		AddEmployee_Page.txt_FullName().clear();
        AddEmployee_Page.txt_FullName().sendKeys(sFullName+"_updt");
        // Printing the logs for what we have just performed
        Log.info(sFullName+" is entered in Full Name text box" );
        Thread.sleep(2000);
        
               
        String sIdentificationType = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Dependent_IdentificationType);       
        AddEmployee_Page.dp_IdentificationType().sendKeys(sIdentificationType+"_updt");
        // Printing the logs for what we have just performed
        Log.info(sIdentificationType+" is entered in Entered in idendification type text box" );
        Thread.sleep(2000);
        
        
        String sIdentification = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Identification);
        AddEmployee_Page.txt_Identification().clear();
        AddEmployee_Page.txt_Identification().sendKeys(sIdentification+"_updt");
        // Printing the logs for what we have just performed
        Log.info(sIdentification+" is entered in Entered in idendificatio text box" );
        Thread.sleep(2000);
        	
        
        String sBirthdate = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_BirthDate);
        AddEmployee_Page.dt_DateOfBirth().clear();
        AddEmployee_Page.dt_DateOfBirth().sendKeys(sBirthdate);
        // Printing the logs for what we have just performed
        Log.info(sBirthdate+" is entered in Entered in Birth day text box" );
        Thread.sleep(2000);
        
        
        String sEntity = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Entity);
        AddEmployee_Page.dp_Entity().sendKeys(sEntity);
        // Printing the logs for what we have just performed
        Log.info(sEntity+" is entered in Entered in idendificatio text box" );
        Thread.sleep(2000);
        
        
        String sDateofHire = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_DateOfHire);
        AddEmployee_Page.dt_DateOfHire().clear();
        AddEmployee_Page.dt_DateOfHire().sendKeys(sDateofHire);
        // Printing the logs for what we have just performed
        Log.info(sDateofHire+" is entered in Entered in idendificatio text box" );
        Thread.sleep(2000);
        
        
        String sEmail = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Email);
        AddEmployee_Page.txt_Email().clear();
        AddEmployee_Page.txt_Email().sendKeys(sEmail);
        // Printing the logs for what we have just performed
        Log.info(sEmail+" is entered in Entered in idendificatio text box" );
        Thread.sleep(3000);
        
        AddEmployee_Page.tab_BankDetail().click();
        Thread.sleep(5000);
        
        String sBankName = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_BankName );
        AddEmployee_Page.dp_BankName().sendKeys(sBankName);
        // Printing the logs for what we have just performed
        Log.info(sBankName+" is entered in Full Name text box" );
        Thread.sleep(2000);
        
        
        String sBranchCode= ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Branchcode );
        AddEmployee_Page.txbx_BranchCode().clear();
        AddEmployee_Page.txbx_BranchCode().sendKeys(sBranchCode);
        // Printing the logs for what we have just performed
        Log.info(sBranchCode+" is entered in Full Name text box" );
        Thread.sleep(2000);
		
        
        String sBankAccountNo= ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_BankAccountNo );
        AddEmployee_Page.txbx_BankAccountNo().clear();
        AddEmployee_Page.txbx_BankAccountNo().sendKeys(sBankAccountNo+"UPDT");
        // Printing the logs for what we have just performed
        Log.info(sBankAccountNo+" is entered in Full Name text box" );
        Thread.sleep(2000);
       
        
        AddEmployee_Page.tab_Child().click();
        Thread.sleep(5000);


		String sdp_Relationship = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col__Relationship );
	    AddEmployee_Page.dp_UpdtDependentRelationship().sendKeys(sdp_Relationship);
	    // Printing the logs for what we have just performed
	    Log.info(sdp_Relationship+" is selected in relationship drop down text box" );
	    Thread.sleep(2000);
		
		
        String sDependent_FullName = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Dependent_FullName );
        AddEmployee_Page.txbx_UpdtDependentFullName().clear();
        AddEmployee_Page.txbx_UpdtDependentFullName().sendKeys(sDependent_FullName+"_updt");
        // Printing the logs for what we have just performed
        Log.info(sDependent_FullName+" is entered in Full Name text box" );
        Thread.sleep(2000);
		
        	
        String sDependent_IdentificatioType = ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Dependent_IdentificationType );
        AddEmployee_Page.dp_UpdtIdentificationType().sendKeys(sDependent_IdentificatioType);
        // Printing the logs for what we have just performed
        Log.info(sDependent_IdentificatioType+" is selected in Identification type" );
        Thread.sleep(2000);
        
        
        String sDependent_Identification= ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Dependent_Identification);
        AddEmployee_Page.txbx_UpdtIdentification().clear();
        AddEmployee_Page.txbx_UpdtIdentification().sendKeys(sDependent_Identification+"_updt");
        // Printing the logs for what we have just performed
        Log.info(sDependent_Identification+" is Enter in Identification text box " );
        Thread.sleep(2000);
        
        
        String sDependent_BirthDate= ExcelUtils.getCellData(iTestCaseRow, EmployeeData.Col_Dependent_BirthDate);
        AddEmployee_Page.dt_UpdtBirthDate().clear();
        AddEmployee_Page.dt_UpdtBirthDate().sendKeys(sDependent_BirthDate);
        // Printing the logs for what we have just performed
        Log.info(sDependent_BirthDate+" is selected as Date of birth" );
        Thread.sleep(2000);
        
        AddEmployee_Page.btn_SaveChanges().click();
		Thread.sleep(2000);
        
		AddEmployee_Page.success_EntityOk().click();
		Thread.sleep(2000);
		}
        
}
        
