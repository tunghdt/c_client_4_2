GridDB C�N���C�A���g

## �T�v

GridDB C�N���C�A���g��C����p�̃C���^�t�F�[�X��񋟂��܂��B  
�܂��A���̃��|�W�g���ɂ͊ȒP�ȃT���v���v���O����������܂��B  
�ڍׂ�API���t�@�����X��API(C����)�̏͂��Q�Ƃ��Ă��������B

## �����

�ȉ��̊���C�N���C�A���g�̃r���h�ƃT���v���v���O�����̎��s���m�F���Ă��܂��B

    OS: CentOS 7.6(x64) (gcc 4.8.5), Windows 10(x64) (VS2017)
    GridDB server: V4.2 CE(Community Edition), CentOS 7.6(x64)

## �N�C�b�N�X�^�[�g(CentOS)

### C�N���C�A���g�̃r���h

    $ cd client/c
    $ ./bootstrap.sh
    $ ./configure
    $ make 
    
�����s����ƁAbin�t�H���_�̉��Ɉȉ��̃t�@�C���⃊���N���쐬����܂��B

    libgridstore.so
	libgridstore.so.0
	libgridstore.so.0.0.0

### �T���v���v���O�����̎��s
���O��GridDB�T�[�o���N�����Ă����K�v������܂��B

    $ cp client/c/sample/sample1.c .
    $ gcc -I./client/c/include -L./bin sample1.c -lgridstore
    $ export LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:./bin
    $ ./a.out <GridDB notification address(default is 239.0.0.1)> <GridDB notification port(default is 31999)>
      <GridDB cluster name> <GridDB user> <GridDB password>
      -->Person: name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]

## �N�C�b�N�X�^�[�g(Windows)

### C�N���C�A���g�̃r���h

client.sln�t�@�C�����N���b�N����VS���N����Aclient�v���W�F�N�g���r���h���Ă��������B

bin/x64�t�H���_�̉��Ɉȉ��̃t�@�C�����쐬����܂��B

    gridstore_c.dll
    gridstore_c.lib

### �T���v���v���O�����̎��s
���O��GridDB�T�[�o���N�����Ă����K�v������܂��B

client.sln�t�@�C�����N���b�N����VS���N����Asample�v���W�F�N�g���r���h����ƁAbin/x64�t�H���_�̉���sample.exe�t�@�C�����쐬����܂��B

    > sample.exe sample1 en <GridDB notification address(default is 239.0.0.1)> <GridDB notification port(default is 31999)>
      <GridDB cluster name> <GridDB user> <GridDB password>
      -->Person: name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]


(�ǉ����)
- client/c/include�t�H���_�̉��ɁA�r���h�Ɏg����gridstore.h�t�@�C��������܂��B  
- client/c/sample�t�H���_�̉��ɁA�T���v���v���O����������܂��B

## �h�L�������g
  �ڍׂ͈ȉ��̃h�L�������g���Q�Ƃ��Ă��������B
  - [API���t�@�����X](https://griddb.github.io/griddb_nosql/manual/GridDB_API_Reference_ja.html)

��C�N���C�A���g(Community Edition)�ł͋�Ԍ^�͗��p�ł��܂���B  

## �R�~���j�e�B
  * Issues  
    ����A�s��񍐂�issue�@�\�������p���������B
  * PullRequest  
    GridDB Contributor License Agreement(CLA_rev1.1.pdf)�ɓ��ӂ��Ē����K�v������܂��B
    PullRequest�@�\�������p�̏ꍇ��GridDB Contributor License Agreement�ɓ��ӂ������̂Ƃ݂Ȃ��܂��B

## ���C�Z���X
  C�N���C�A���g�̃��C�Z���X��Apache License, version 2.0�ł��B  
  �T�[�h�p�[�e�B�̃\�[�X�ƃ��C�Z���X�ɂ��Ă�3rd_party/3rd_party.md���Q�Ƃ��������B
