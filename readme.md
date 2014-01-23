������ 2 - .msi �����
============================================================

������ ������ - .msi ����� ��� ������������ � ������ ������
[������������ ��������� ��� ������� ������������������ ��� ��������� � �������
���������������� ����������� �������� ������ 2][������ 2].

� ��������� ������ � ����� �������� ��������� ��������:
- ������ 2-10� ��� ���������� �������, ��������� � �������� ���������������
������������� ����������� ��������, ������� ������� ������� 10.5-10.55 ���;
- ������ 2-24� ��� ���������� �������, ��������� � �������� ���������������
������������� ����������� ��������, ������� ������� ������� 24.5-24.25 ���.

����������� ��� ������ .msi ������
----------------------------------

��� �������� ��������� � ����� � ��������� ������ ������ ����������� ��������� ��������:

- Microsoft Visual Studio 2012 Shell:
	- [MS Visual Studio 2012 Shell Isolated][]
	- [MS Visual Studio 2012 Shell Integrated][]
- [Windows Installer XML Toolset - WIX 4.0][WIX]

���������� ���������� ��� ������ � ��������� �������. � ���������� - ������� MS Visual Studio 2012 � ���������������
��������� �������� WiX. ����� ����� ��������� ���� ������� `.sln` � �������� �������.

�������� �������
----------------

### ���������������� ����� ���������

� ����� `bin\Admin image\x86\ru-RU` ������ ������, �������������� � ���� ���������������� ����� ���������.
� ��� ����������� ��������� ������������.

### .msi ����� � ���� ������� �����

� ����� `bin\Single .msi file\x86\ru-RU` ������ .msi ����� � ���� ������� �����.
� ������� �� ����������� ��������, � ������ �������� ������������ ��������� ������������,
����������� �������� � ������ ��������, � ����� ��� ���������.

��� ������������� �������� ���������������� ����� ��������� � ����������� ������������ ������� ���������������
��������� ������� �� ���������� �������:

    msiexec -a "bin\Single .msi file\x86\ru-RU\sapsan2.msi" TARGETDIR="adm\x86"

���������� ���������������� ����� ���������
-------------------------------------------

��� ���������� ���������������� ����� ��������� �������� � ��������� ������������� ��������.

### ALLUSERS

�� ��������� - `"1"`. ��� ��������� `"0"` ����������� ����� ������������ � ������� ������������, � �� � ������� ����������.

### DISABLESHORTCUTS

�� ��������� - `"No"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ������.
��� ������� ������ ������������� ������� ����� �� �������������.

### DISABLEDESKTOPSHORTCUTS

�� ��������� - `"No"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ������ �� ������� �����.
��� `DISABLESHORTCUTS="Yes"` �������� ������� �������� ���� �� ������.

### DISABLEMENUSHORTCUTS

�� ��������� - `"No"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ������ � ����.
��� `DISABLESHORTCUTS="Yes"` �������� ������� �������� ���� �� ������.

### APPLICATIONFOLDER

���� � �����, � ������� ����� ���������� ����������� �������. �� ��������� - `%ProgramFiles(x86)%\STP\RashodomerISO\2.4`.
������������� � �������� �������� ������� �������� ��������� ������ ���� �� ��������� � `%ProgramFiles%`.

### �������

��������� �������� ���������� ���������������� ����� ���������:

	msiexec -a sapsan2.msi DISABLEDESKTOPSHORTCUTS=Yes ALLUSERS=0

������ ��������� ������ ������� ����� ��������� � "������������" �������� �������� �����, � ���������� ���������� ��� ������������
(� �� ��� ����������).

	msiexec -a sapsan2.msi DISABLESHORTCUTS=Yes

������ ��������� ������ ������� ����� ��������� � "������������" ��������.

[������ 2]: http://www.olvia.ru/rus/products.php?s=9
[MS Visual Studio 2012 Shell Isolated]: http://www.microsoft.com/ru-ru/download/details.aspx?id=30670
[MS Visual Studio 2012 Shell Integrated]: http://www.microsoft.com/ru-ru/download/details.aspx?id=30663
[WIX]: http://wixtoolset.org/
