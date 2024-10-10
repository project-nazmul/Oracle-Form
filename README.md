##########################################
DECLARE
	X boolean;
begin
	x := SHOW_LOV('MPO_LIST');
END;
####################################
Declare
		N number;
	Begin
		N:=show_alert('SUCCESSFUL');
	end;
#################################
 WHEN-NEW-FORM-INSTANCE

GO_BLOCK('SD_MPO');
EXECUTE_QUERY;

GO_BLOCK('SD_MPO1');
EXECUTE_QUERY;


GO_BLOCK('SD_FM');
EXECUTE_QUERY;
####################################
#LOGIN
IF :TEXT_ITEM13 = 'NAZMUL' AND :TEXT_ITEM14 = '123456' 
	THEN
	:GLOBAL.USERNAME := 'How are you? Md. Nazmul Khan ';
	CALL_FORM('C:\Users\nazmulkhan\Desktop\Form_Application\HOME_SCREEN.fmx');
ELSE 
	MESSAGE('Incorrect Username/Password');
	MESSAGE('Incorrect Username/Password');
END IF;
##########
CLEAR_FORM;
GO_BLOCK('FF_OPL_VW');
EXECUTE_QUERY;
###########
EXIT_FORM;
##########
:NAME1 := :GLOBAL.USERNAME;
##############
GO_ITEM('BLOCK3.TEXT_ITEM5');
######################
