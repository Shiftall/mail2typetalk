# mail2typetalk
Mail to Typetalk with Mailgun API/GAE

# �g����
secret.yaml.sample���Q�l�ɁAsecret.yaml�������B

* MAILGUN_API_KEY
  * Mailgun��API�L�[
* TYPETALK_CLIENT_ID
  * Typetalk��Client Credential��������AccessToken�ŃA�N�Z�X���邽�߁ACLIENT ID��ݒ�B
  * CLIENT ID�̎擾����[Typetalk API�h�L�������g](https://developer.nulab-inc.com/ja/docs/typetalk/auth/#client)���Q�ƁB
* TYPETALK_BOT_POST_URL
  * �G���[���̃��b�Z�[�W�Ȃǂ�Typetalk�ɓ��e���邽�߂�BOT�pPOST URL�ݒ�B
    * ������͏�LCLIENT ID�Ƃ͕ʂŁA�g�s�b�N����BOT���쐬���Ă���URL��ݒ�B
  * ��p�̃g�s�b�N������ĊǗ��҂����������悤�ɂ��Ă����̂��z��B
* GOOGLE_APPLICATION_CREDENTIALS
  * Cloud Datastore���g�����߂̔F�ؗp�t�@�C���BGoogle Cloud�Ő������ꂽjson�t�@�C�����w��B
* CLOUD_STORE_KIND
  * Datastore���kind ���Ɏw��͂Ȃ��̂ŁA�C�ӂ̖��O��OK�B

���̏�ŁA
```bash
$ python3 -m venv env
$ source env/bin/activate
$ pip install -r requirements.txt
$ python main.py
�Ń��[�J���ŃT�[�o���N���ł���B�\�ł���΁A���̃T�[�o��Mailgun�����POST���͂��悤�ɂ���΃e�X�g���₷���B

GAE�ւ̃f�v���C�Ȃǂ́AGAE�h�L�������g���Q�ƁB
