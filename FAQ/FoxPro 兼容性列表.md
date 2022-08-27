原帖地址：https://www.xsharp.info/itm-help/foxpro-compatibility-list

**翻译：xinjie  2020.06.15**

更新：2020.09.21 for Ver:2.6.0.0


有一些 Foxer 希望能提供一个列表，以明确了解 X＃ 支持哪些 FoxPro 的功能。

下面的列表表示了版本 2.6 的状态。

FoxPro 中的一些命令内置于编译器中。 我们称之为语句（statements）。

其他的则通过所谓的用户自定义命令（UDCs）来实现。 它们在外部头文件中定义。 编译器将它们编译为运行时库中的函数调用。 例如，SEEK 命令转换为对 DbSeek（）函数的调用，而 SKIP 命令转换为对 DbSkip（）函数的调用。

此列表会随着对 VFP 支持的完善而不断更新。

# 语句（内置于编译器）

语句 |可用状态
-|-
&	 |支持
?和??	 |支持
***???***	 |***不支持***
\和\\	 |支持
=	 |支持
DECLARE	 |支持
DEFINE CLASS	 |支持
DIMENSION	 |支持
DO CASE	 |支持
DO	 |支持
DO WHILE	 |支持
EXIT	 |支持
FOR .. ENDFOR	 |支持
FOR EACH .. ENDFOR	 |支持
IF .. ELSE .. ENDIF	 |支持
LOCAL	 |支持.
LOOP	 |支持
LPARAMETERS	 |支持
MEMVAR	 |支持
PARAMETERS	 |支持
PRIVATE	 |支持
PUBLIC	 |支持
RETURN	 |支持
TEXT .. ENDTEXT	 |支持
TRY .. CATCH .. FINALLY	 |支持
WITH .. ENDWITH	 |支持

# 数据库和工作区命令
其中一些仅适用于类似 VFP 的交互式环境。

使用 UDC 和 X＃ 运行时中已经可用的功能，可以实现某些不支持的命令。

语句	|可用状态	|语句	|可用状态
-|-|-|-
APPEND FROM	 |支持	|APPEND From Array	|已实现
AVERAGE	|支持	|**BEGIN TRANSACTION**	|**未实现**
CLOSE	|支持	|**BLANK**	|**未实现**
CONTINUE	|支持	|**CALCULATE**	|**未实现**
COPY FILE	|支持	|COPY To Array	|已实现
COPY STRUCTURE	|支持	|**DELETE - SQL**	|**未实现**
COPY STRUCTURE EXTENDED	|支持	|**DROP TABLE/VIEW**	|**未实现**
COPY TO	 |支持	 |**EXPORT**	|**未实现**
COUNT	|支持	|**FLUSH**	|**未实现**
DELETE	|支持	|**FREE TABLE**	|**未实现**
DELETE FILE	 |支持	|GATHER	|已实现
ERASE	|支持	|**IMPORT**	|**未实现**
GO 和 GOTO	|支持	|**INSERT - SQL**	|**未实现**
INDEX ON	|支持	|**OPEN DATABASE**	|**未实现**
LOCATE	|支持	|**REPLACE FROM ARRAY**	|**未实现**
PACK	|支持	|SCATTER	|已实现
RECALL	|支持	|**SELECT - SQL**	|**未实现**
REINDEX	|支持	|**UPDATE - SQL**	|**未实现**
REPLACE	|支持	|**VALIDATE DATABASE**	|**未实现**
SCAN .. ENDSCAN	|支持		
SEEK	|支持		
SELECT	|支持		
SET (variations)	|**部分支持**
SKIP	|支持		
SORT	|支持		
SUM	|支持		
TOTAL	|支持		
UNLOCK	|支持		
USE	|支持		
ZAP	|支持	

# 其他命令

这些命令大多数与 VFP IDE 或 VFP UI 类有关

语句	|可用状态		|语句	|可用状态		|语句	|可用状态
-|-|-|-|-|-
CLEAR	|支持		|BEGIN TRANSACTION	|未实现		|ACTIVATE (all variations)	|不适用
DEFINE (other variations)	|支持		|CD / CHDIR	|未实现		|APPEND (other variations)	|不适用
ERASE	|支持		|COPY (other variations)	|未实现		|BROWSE	|不适用
NODEFAULT	|支持		|EJECT	|未实现		|BUILD	|不适用
QUIT	|支持  		|ERROR	|未实现		|CANCEL	|不适用
RELEASE memvars	|支持		|EXPORT	|未实现		|CHANGE	|不适用
RESTORE FROM	|支持		|FLUSH	|未实现		|CLOSE MEMO	|不适用
RUN	|支持		|HELP	|未实现		|COMPILE	|不适用
SAVE TO	|支持		|KEYBOARD	|未实现		|CREATE (all variations)	|不适用
SCROLL	|支持		|LABEL	|未实现		|DEACTIVATE (all variations)	|不适用
SET (global state)	|部分支持		|MD 和 MKDIR	|已实现		|DEBUG	|不适用
STORE	 |支持	  |ON (all variations)	 |未实现		 |DEBUGOUT	 |不适用
WAIT	 |支持		 |PRINTJOB	 |未实现		 |DELETE (other variations)	 |不适用
-|-|PUSH (all variations)	 |未实现		 |DISPLAY (all variations)	 |不适用
-|-|RD 和 RMDIR	 |未实现		 |DO FORM	 |不适用
-|-|RELEASE (other variations)	 |未实现		 |DOCK	 |不适用
-|-|REMOVE (all variations)	 |未实现		 |DOEVENTS	 |不适用
-|-|RENAME (all variations)	 |未实现		 |EXTERNAL	 |不适用
-|-|REPORT FORM	 |未实现		 |GETEXPR	 |不适用
-|-|RESTORE (other variations)	 |未实现		 |HIDE (all variations)	 |不适用
-|-|ROLLBACK	 |未实现		 |LIST (all variations)	 |不适用
-|-|TYPE	 |未实现		 |MENU	 |不适用
-|-|-|-|MODIFY (all variations)	 |不适用
-|-|-|-|PLAY MACRO	 |不适用
-|-|-|-|POP (all variations)	 |不适用
-|-|-|-|READ EVENTS	 |不适用
-|-|-|-|RESUME	 |不适用
-|-|-|-|RETRY	 |不适用
-|-|-|-|SAVE (other variations)	 |不适用
-|-|-|-|SHOW (all variations)	 |不适用
-|-|-|-|SIZE (all variations)	 |不适用
-|-|-|-|SUSPEND	 |不适用
-|-|-|-|ZOOM WINDOW	 |不适用

# 函数

X＃ 中已经提供了大多数与工作区相关的函数以及字符串转换和处理的函数。

完全支持的函数	 |具有不同参数的函数（参数相比于VFP可能更多或者更少）	 |暂时不可用的函数	 |不会被支持的函数
-|-|-|-
ABS( )	 |ACOPY( )	 |ACLASS( )	 |ADLLS( )
ACOS( )	 |ADIR( )	 |ADATABASES( )	 |ADOCKSTATE( )
ADEL( )	 |AFIELDS( )	 |ADBOBJECTS( )	 |AERROR( )
ALIAS( )	 |AINS( )	 |ADDBS( )（已可用）	 |AEVENTS( )
ASIN( )	 |ALEN( )	 |ADDPROPERTY( )（已可用）	 |AFONT( )
ATAN( )	 |ALLTRIM( )	 |AELEMENT( )	 |AGETCLASS( )
ATCLINE( )	 |ASC( )	 |AGETFILEVERSION( )	 |AINSTANCE( )
ATLINE( )	 |ASCAN( )	 |ALINES( )	 |ALANGUAGE( )
ATN2( )	 |ASORT( )	 |AMEMBERS( )	 |AMOUSEOBJ( )
BETWEEN( )	 |AT( )	 |ANETRESOURCES( )	 |APROCINFO( )
BOF( )	 |ATC( )	 |APRINTERS( )	 |ASELOBJ( )
CDOW( )	 |ATCC( )	 |ASESSIONS( )	 |AVCXCLASSES( )
CHR( )	 |CHRSAW( )	 |ASQLHANDLES( )（已可用）	 |BAR( )
CMONTH( )	 |CHRTRAN( )	 |ASTACKINFO( )	 |BARCOUNT( )
COS( )	 |CHRTRANC( )	 |ASUBSCRIPT( )	 |BARPROMPT( )
CREATEOBJECT( )	 |CLEARRESULTSET( )	 |AT_C( )（已可用）	 |BINDEVENT( )
CTOD( )	 |CNTBAR( )	 |ATAGINFO( )	 |COMARRAY( )
CURDIR( )	 |CNTPAD( )	 |AUSED( )	 |COMCLASSINFO( )
DELETED( )	 |COL( )	 |BINTOC( )（已可用）	 |COMPROP( )
DOW( )	 |DAY( )	 |BITAND( )	 |COMRETURNERROR( )
DTOC( )	 |DBF( )	 |BITCLEAR( )	 |CPCURRENT( )
DTOR( )	 |DIRECTORY( )	 |BITLSHIFT( )	 |CREATEBINARY( )
DTOS( )	 |DISKSPACE( )	 |BITNOT( )	 |DDEAbortTrans( )
EMPTY( )	 |EVALUATE( )	 |BITOR( )	 |DDEAdvise( )
EOF( )	 |INT( )	 |BITRSHIFT( )	 |DDEEnabled( )
EXP( )	 |MAX( )	 |BITSET( )	 |DDEExecute( )
FCHSIZE( )	 |MCOL( )	 |BITTEST( )	 |DDEInitiate( )
FCLOSE( )	 |MDOWN( )	 |BITXOR( )	 |DDELastError( )
FCOUNT( )	 |MIN( )	 |CANDIDATE( )	 |DDEPoke( )
FCREATE( )	 |OBJNUM( )	 |CAPSLOCK( )	 |DDERequest( )
FDATE( )	 |OBJVAR( )	 |CAST( )	 |DDESetOption( )
FEOF( )	 |OEMTOANSI( )	 |CDX( )（已可用）	 |DDESetService( )
FERROR( )	 |SQRT( )	 |CEILING( )	 |DDESetTopic( )
FFLUSH( )	 |STRTRAN( )	 |COMPOBJ( )	 |DDETerminate( )
FGETS( )	 |TRIM( )	 |COMPILE()	 |EDITSOURCE( )
FILE( )	 |TYPE( )	 |CPCONVERT( )	 |ERROR( )
FLOCK( )		 |-|CPDBF( )（已可用）	 |EVENTHANDLER( )
FLOOR( )		 |-|CREATEOBJECTEX( )	 |FKLABEL( )
FOPEN( )		 |-|CREATEOFFLINE( )	 |FKMAX( )
FOUND( )		 |-|CTOBIN( )	 |GETBAR( )
FPUTS( )		 |-|CTOT( )	 |GETINTERFACE( )
FREAD( )		 |-|CURSORGETPROP( )	 |GETPAD( )
FSEEK( )		 |-|CURSORSETPROP( )	 |GETPEM( )
FSIZE( )		 |-|CURSORTOXML( )	 |HOME( )
FTIME( )		 |-|CURVAL( )	 |INKEY( )
FWRITE( )		 |-|DATE( )（已可用）	 |ISLEADBYTE( )
GETENV( )		 |-|DATETIME( )（已可用）	 |LASTKEY( )
HEADER( )		 |-|DBALIAS( )	 |MEMORY( )
ICASE( )		 |-|DBC( )	 |MENU( )
IIF()		 |-|DBGETPROP( )	 |MESSAGE( )
INLIST( )		 |-|DBSETPROP( )	 |MRKBAR( )
ISALPHA( )		 |-|DBUSED( )	 |MRKPAD( )
ISDIGIT( )		 |-|DEFAULTEXT( )	 |MROW( )
ISLOWER( )		 |-|DESCENDING( )（已可用）	 |MWINDOW( )
ISUPPER( )		 |-|DIFFERENCE( )	 |OBJTOCLIENT( )
LEFT( )		 |-|DisplayPath( )	 |ON( )
LEN( )		 |-|DMY( )（已可用）	 |PAD( )
LIKE( )		 |-|DODEFAULT( )	 |PADPROMPT( )
LOG( )		 |-|DRIVETYPE( )	 |PARAMETERS( )
LOG10( )		 |-|DROPOFFLINE( )	 |PEMSTATUS( )
LOWER( )		 |-|DTOT( )	 |POPUP( )
LTRIM( )		 |-|EVL( )	 |PRINTSTATUS( )
LUPDATE( )		 |-|EXECSCRIPT( )	 |PRMBAR( )
MEMLINES( )		 |-|FIELD( )（已可用）	 |PRMPAD( )
MLINE( )		 |-|FILETOSTR( )（已可用）	 |PROMPT( )
MOD( )		 |-|FILTER( )（已可用）	 |RDLEVEL( )
MONTH( )		 |-|FLDCOUNT( )（已可用）	 |READKEY( )
OCCURS( )		 |-|FLDLIST( )	 |SCOLS( )
OS( )		 |-|FONTMETRIC( )	 |SKPBAR( )
PADL( )		 |-|FOR( )（已可用）	 |SKPPAD( )
PADR( )		 |-|FORCEEXT( )（已可用）	 |SROWS( )
PADC( )		 |-|FORCEPATH( )（已可用） |UNBINDEVENTS( )
PCOUNT( )		 |-|FULLPATH( )	 |UPDATED( )
PI( )		 |-|FV( )	 |VARREAD( )
PROPER( )		 |-|GETAUTOINCVALUE( )	 |WBORDER( )
RAND( )		 |-|GETCOLOR( )	 |WCHILD( )
RAT( )		 |-|GETCP( )	 |WCOLS( )
RATLINE( )		 |-|GETDIR( )	 |WDOCKABLE( )
RECCOUNT( )		 |-|GETFILE( )	 |WEXIST( )
RECNO( )		 |-|GETFLDSTATE( )	 |WFONT( )
RECSIZE( )		 |-|GETFONT( )	 |WLAST( )
REPLICATE( )		 |-|GETNEXTMODIFIED( )	 |WLCOL( )
RGB( )		 |-|GETOBJECT( )	 |WLROW( )
RIGHT( )		 |-|GETPICT( )	 |WMAXIMUM( )
RLOCK( )		 |-|GETPRINTER( )	 |WMINIMUM( )
ROUND( )		 |-|GETRESULTSET( )	 |WONTOP( )
ROW( )		 |-|GETWORDCOUNT( )（已可用）	 |WOUTPUT( )
RTOD( )		 |-|GETWORDNUM( )（已可用）	 |WPARENT( )
RTRIM( )		 |-|GETCURSORADAPTER( )	 |WREAD( )
SECONDS( )		 |-|GOMONTH( )（已可用）	 |WROWS( )
SET( )		 |-|HOUR( )（已可用）	 |WTITLE( )
SIN( )		 |-|ID( )	 |WVISIBLE( )
SOUNDEX( )		 |-|IDXCOLLATE( )（已可用）	 |-
SPACE( )		 |-|IMESTATUS( )	 |-
STR( )		 |-|INDBC( )	 |-
STUFF( )		 |-|INDEXSEEK( )	 |-
SUBSTR( )		 |-|INPUTBOX( )	 |-
TAN( )		 |-|INSMODE( )	 |-
TIME( )		 |-|ISBLANK( )	 |-
TRANSFORM( )		 |-|ISCOLOR( )（已可用）	 |-
UPPER( )		 |-|ISEXCLUSIVE( )	 |-
USED( )		 |-|ISFLOCKED( )（已可用）	 |-
VAL( )		 |-|ISMEMOFETCHED( )	 |-
VERSION( )		 |-|ISMOUSE( )	 |-
YEAR( )		 |-|ISNULL( )	 |-
-|-|ISPEN( )	 |-
-|-|ISREADONLY( )（已可用）	 |-
-|-|ISRLOCKED( )（已可用）	 |-
-|-|ISTRANSACTABLE( )	 |-
-|-|JUSTDRIVE( )（已可用）	 |-
-|-|JUSTEXT( )（已可用）	 |-
-|-|JUSTFNAME( )（已可用）	 |-
-|-|JUSTPATH( )（已可用）	 |-
-|-|JUSTSTEM( )（已可用）	 |-
-|-|KEY( )（已可用）	 |-
-|-|KEYMATCH( )	 |-
-|-|LEFTC( )（已可用）	 |-
-|-|LENC( )（已可用）	 |-
-|-|LIKEC( )（已可用）	 |-
-|-|LINENO( )	 |-
-|-|LOADPICTURE( )	 |-
-|-|LOCFILE( )	 |-
-|-|LOCK( )	 |-
-|-|LOOKUP( )	 |-
-|-|MAKETRANSACTABLE( )	 |-
-|-|MDX( )（已可用）	 |-
-|-|MDY( )（已可用）	 |-
-|-|MESSAGEBOX( )（已可用）	 |-
-|-|MINUTE( )（已可用）	 |-
-|-|MTON( )（已可用）	 |-
-|-|NDX( )	 |-
-|-|NEWOBJECT( )	 |-
-|-|NORMALIZE( )	 |-
-|-|NTOM( )（已可用）	 |-
-|-|NUMLOCK( )	 |-
-|-|NVL( )	 |-
-|-|OLDVAL( )	 |-
-|-|ORDER( )（已可用）	 |-
-|-|PAYMENT( )	 |-
-|-|PCOL( )	 |-
-|-|PRIMARY( )	 |-
-|-|PROGRAM( )	 |-
-|-|PROW( )	 |-
-|-|PRTINFO( )	 |-
-|-|PUTFILE( )	 |-
-|-|PV( )	 |-
-|-|QUARTER( )（已可用）	 |-
-|-|RAISEEVENT( )	 |-
-|-|RATC( )（已可用）	 |-
-|-|REFRESH( )	 |-
-|-|RELATION( )（已可用）	 |-
-|-|REMOVEPROPERTY( )（已可用）	 |-
-|-|REQUERY( )	 |-
-|-|RGBSCHEME( )	 |-
-|-|RIGHTC( )（已可用）	 |-
-|-|SAVEPICTURE( )	 |-
-|-|SCHEME( )	 |-
-|-|SEC( )（已可用）	 |-
-|-|SEEK( )	 |-
-|-|SELECT( )（已可用）	 |-
-|-|SETFLDSTATE( )	 |-
-|-|SETRESULTSET( )	 |-
-|-|SIGN( )	 |-
-|-|SQLCANCEL( )（已可用）	 |-
-|-|SQLCOLUMNS( )（已可用）	 |-
-|-|SQLCOMMIT( )（已可用）	 |-
-|-|SQLCONNECT( )（已可用）	 |-
-|-|SQLDISCONNECT( )（已可用）	 |-
-|-|SQLEXEC( )（已可用）	 |-
-|-|SQLGETPROP( )（已可用）	 |-
-|-|SQLIDLEDISCONNECT( )（已可用）	 |-
-|-|SQLMORERESULTS( )（已可用）	 |-
-|-|SQLPREPARE( )（已可用）	 |-
-|-|SQLROLLBACK( )（已可用）	 |-
-|-|SQLSETPROP( )（已可用）	 |-
-|-|SQLSTRINGCONNECT( )（已可用）	 |-
-|-|SQLTABLES( )（已可用）	 |-
-|-|STRCONV( )	 |-
-|-|STREXTRACT( )	 |-
-|-|STRTOFILE( )（已可用）	 |-
-|-|STUFFC( )（已可用）	 |-
-|-|SUBSTRC( )（已可用）	 |-
-|-|SYSMETRIC( )	 |-
-|-|TABLEREVERT( )	 |-
-|-|TABLEUPDATE( )	 |-
-|-|TAG( )（已可用）	 |-
-|-|TAGCOUNT( )（已可用）	 |-
-|-|TAGNO( )（已可用）	 |-
-|-|TARGET( )（已可用）	 |-
-|-|TEXTMERGE( )	 |-
-|-|TTOC( )	 |-
-|-|TTOD( )（已可用）	 |-
-|-|TXNLEVEL( )	 |-
-|-|TXTWIDTH( )	 |-
-|-|UNIQUE( )（已可用）	 |-
-|-|VARTYPE( )（已可用）	 |-
-|-|WEEK( )（已可用）	 |-
-|-|XMLTOCURSOR( )	 |-
-|-|XMLUPDATEGRAM( )	
