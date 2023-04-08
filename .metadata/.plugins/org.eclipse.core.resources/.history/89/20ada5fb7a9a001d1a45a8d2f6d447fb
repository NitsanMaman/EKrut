package UnitTest;

import static org.junit.Assert.*;
import static org.mockito.Mockito.*;

import java.util.ArrayList;

import org.junit.Before;
import org.junit.Test;

import gui.ReportScreens.ReportsMainScreenController;
import javafx.scene.input.MouseEvent;

public class ReportsMainScreenControllerTest {
	   private ReportsMainScreenController mockReportsMainScreenController;
	   private MouseEvent event;
	@Before
	public void setUp() throws Exception {
		mockReportsMainScreenController = spy(new ReportsMainScreenController());
	}

	  // Check Functionality: testing clickShowReport case that no month has been chosen - NULL month
	  // Input Data: (null) getMonth()
	  // Expected Result: "You didn't choose Month!"
	  @Test
	  public void TestclickShowReportNULLMonth() {
		doReturn(null).when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		String expected = "You didn't choose Month!";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that no year has been chosen - NULL year
	  // Input Data: "10" (String) getMonth(), (null) getYearComboBox()
	  // Expected Result: "You didn't choose Year!"
	  @Test
	  public void TestclickShowReportNULLYear() {
		doReturn("10").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn(null).when(mockReportsMainScreenController).getYearComboBox();
		String expected = "You didn't choose Year!";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing  clickShowReport case that no type has been chosen - NULL type
	  // Input Data: "10" (String) getMonth(), "2022" (String) getYearComboBox() ,(null) getType()
	  // Expected Result: "You didn't choose Report Type!"
	  @Test
	  public void TestclickShowReportNULLType() {
		doReturn("10").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn(null).when(mockReportsMainScreenController).getType();
		String expected = "You didn't choose Report Type!";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that no Location has been chosen - NULL Location and the comboBox was visible
	  // Input Data: "10" (String) getMonth(),"2022" (String) getYearComboBox() ,"Inventory" (String) getType() ,(null) getLocation() ,(int) getLocationFlag() 
	  // Expected Result: "You didn't choose Location !"
	  @Test
	  public void TestclickShowReportNULLLocationFlag1() {
		doReturn("10").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn("Inventory").when(mockReportsMainScreenController).getType();
		doReturn(null).when(mockReportsMainScreenController).getLocation();
		doReturn(1).when(mockReportsMainScreenController).getLocationFlag();
		String expected = "You didn't choose Location !";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that no Location has been chosen - NULL Location and the comboBox was invisible
	  // Input Data: "10" (String) getMonth(), "2022" (String) getYearComboBox() , "Inventory" (String) getType() ,(null) getLocation() , 0 (int) getLocationFlag() , (null) getMachineID(), 1 (int) getMachineIDFlag()
	  // Expected Result: "You didn't choose Machine ID!"
	  @Test
	  public void TestclickShowReportNULLLocationFlag0() {
		doReturn("10").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn("Inventory").when(mockReportsMainScreenController).getType();
		doReturn(null).when(mockReportsMainScreenController).getLocation();
		doReturn(0).when(mockReportsMainScreenController).getLocationFlag();
		doReturn(null).when(mockReportsMainScreenController).getMachineID();
		doReturn(1).when(mockReportsMainScreenController).getMachineIDFlag();
		String expected = "You didn't choose Machine ID!";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that no MachineID has been chosen - NULL MachineID and the comboBox was visible
	  // Input Data:"10" (String) getMonth(),"2022" (String) getYearComboBox() ,"Inventory" (String) getType() , "north" (String) getLocation() ,0 (int) getLocationFlag(), (null) getMachineID(),1 (int) getMachineIDFlag()
	  // Expected Result: "You didn't choose Machine ID!"
	  @Test
	  public void TestclickShowReportNULLMachineIDFlag1() {
		doReturn("10").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn("Inventory").when(mockReportsMainScreenController).getType();
		doReturn("north").when(mockReportsMainScreenController).getLocation();
		doReturn(0).when(mockReportsMainScreenController).getLocationFlag();
		doReturn(null).when(mockReportsMainScreenController).getMachineID();
		doReturn(1).when(mockReportsMainScreenController).getMachineIDFlag();
		String expected = "You didn't choose Machine ID!";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that no MachineID has been chosen - NULL MachineID and the comboBox was invisible
	  // Input Data:"1" (String) getMonth(),"2022" (String) getYearComboBox() ,"Inventory" (String) getType() ,"north" (String) getLocation(),0 (int) getLocationFlag(), (null) getMachineID() ,0 (int) getMachineIDFlag()
	  // Expected Result: "Report not found"
	  @Test
	  public void TestclickShowReportNULLMachineIDFlag0() {
		doReturn("1").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn("Inventory").when(mockReportsMainScreenController).getType();
		doReturn("north").when(mockReportsMainScreenController).getLocation();
		doReturn(0).when(mockReportsMainScreenController).getLocationFlag();
		doReturn(null).when(mockReportsMainScreenController).getMachineID();
		doReturn(0).when(mockReportsMainScreenController).getMachineIDFlag();
		doNothing().when(mockReportsMainScreenController).saveChatClientData();
		ArrayList<String> monthYearMachine = new ArrayList<>();
		monthYearMachine.add("1");
		monthYearMachine.add("2022");
		doReturn("Report not found").when(mockReportsMainScreenController).inventoryReportCase(monthYearMachine,null);
		String expected = "Report not found";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that show report Not Found when valid data were chosen!
	  // Input Data:"1" (String) getMonth(),"2022" (String) getYearComboBox() ,"Inventory" (String) getType() ,"north" (String) getLocation(),0 (int) getLocationFlag(),"NOR1" (String) getMachineID() ,0 (int) getMachineIDFlag()
	  // Expected Result: "Report not found"
	  @Test
	  public void TestclickShowReportNotFound() {
		doReturn("1").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn("Inventory").when(mockReportsMainScreenController).getType();
		doReturn("north").when(mockReportsMainScreenController).getLocation();
		doReturn(0).when(mockReportsMainScreenController).getLocationFlag();
		doReturn("NOR1").when(mockReportsMainScreenController).getMachineID();
		doReturn(0).when(mockReportsMainScreenController).getMachineIDFlag();
		doNothing().when(mockReportsMainScreenController).saveChatClientData();
		ArrayList<String> monthYearMachine = new ArrayList<>();
		monthYearMachine.add("1");
		monthYearMachine.add("2022");
		doReturn("Report not found").when(mockReportsMainScreenController).inventoryReportCase(monthYearMachine,null);
		String expected = "Report not found";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
	  
	  // Check Functionality: testing clickShowReport case that inventory report successfully view
	  // Input Data:"10" (String) getMonth(),"2022" (String) getYearComboBox() ,"Inventory" (String) getType() ,"north" (String) getLocation(),0 (int) getLocationFlag(), "NOR1" (String) getMachineID() ,0 (int) getMachineIDFlag()
	  // Expected Result: "done"
	  @Test
	  public void TestclickShowReportDoneSuccessfull() {
		doReturn("10").when(mockReportsMainScreenController).getMonth();
		doNothing().when(mockReportsMainScreenController).alertHandler(anyString(), anyBoolean());
		doReturn("2022").when(mockReportsMainScreenController).getYearComboBox();
		doReturn("Inventory").when(mockReportsMainScreenController).getType();
		doReturn("north").when(mockReportsMainScreenController).getLocation();
		doReturn(0).when(mockReportsMainScreenController).getLocationFlag();
		doReturn("NOR1").when(mockReportsMainScreenController).getMachineID();
		doReturn(0).when(mockReportsMainScreenController).getMachineIDFlag();
		doNothing().when(mockReportsMainScreenController).saveChatClientData();
		ArrayList<String> monthYearMachine = new ArrayList<>();
		monthYearMachine.add("10");
		monthYearMachine.add("2022");
		doReturn("Report was found").when(mockReportsMainScreenController).inventoryReportCase(monthYearMachine,null);
		doReturn(null).when(mockReportsMainScreenController).fxmlLoader();
		doNothing().when(mockReportsMainScreenController).switchToReport(event,null);
		String expected = "done";
		String result = mockReportsMainScreenController.clickShowReport(event);
		assertEquals(expected, result);
	   }
}
