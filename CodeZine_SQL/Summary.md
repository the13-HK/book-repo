### 3 �l�_���� NULL

- 3 �l�_���Ƃ́A�^(true)�A�U(false)�A�s��(unknown)�� 3 �̒l�����_���B
- NULL �ɂ́A�l���s���ł��邱�Ɓi���m�j��\���Ӗ��ƁA�l�����݂��Ȃ����Ɓi�K�p�s�\�j��\���Ӗ��� 2 ������B
- NULL �Ƃ̔�r���Z�́A��ɕs��(UNKNOWN)�ɂȂ邽�߁ANULL �̔���́AIS NULL �܂��� IS NOT NULL ���g�p����B
- �^�U�l�ɂ����� unknown �� NULL �̈��� UNKNOWN �Ƃ͈قȂ�B
  - unknown �� unknown �̔�r�� TRUE �ɂȂ邪�AUNKNOWN �� UNKNOWN �̔�r�� unknown �ɂȂ�B
    - unknown �͏�Ԃ�\�����̂ł���ATrue�AFalse �Ɠ����x���̂��́B
- �r�����i�r�����j�F���閽�肪�^�ł��邩�U�ł��邩�̂����ꂩ�ł��邱�ƁB
  - 3 �l�_���ł́A�r���������藧���Ȃ��B
  - 3 �l�_���ł́A�^�ł��U�ł��Ȃ��s���ȏ�Ԃ����݂��邽�߁A�r���������藧���Ȃ��B
- CASE ���ɂ����āAWHEN �� �� NULL ���w�肵�Ă��ANULL �Ƃ̔�r�͕s���ɂȂ邽�߁ATHEN �Ŏw�肵���l�̓Z�b�g���ꂸ�AELSE �� �����s�����B
  - ELSE �� ���Ȃ��ꍇ�́ANULL ���Ԃ����B
- NOT IN �� NOT EXISTS �� NULL ���܂ޏꍇ�ɒ��ӂ��K�v�B
  - NOT IN �́ANULL ���܂ޏꍇ�ANULL �Ƃ̔�r�͕s���ɂȂ邽�߁ANULL ���Ԃ����B
  - NOT EXISTS �́ANULL ���܂ޏꍇ�ANULL �Ƃ̔�r�͕s���ɂȂ邽�߁ANULL ���Ԃ���邪�ANULL �͋U�Ƃ��Ĉ����邽�߁ANOT EXISTS �͏�ɐ^�ɂȂ�B
- Null ��h�����߂ɂ�
  - �e�[�u����`�� NOT NULL �����t�^����B
- Oracle �� NULL �� �󕶎� �Ɋւ��郍�[�J�����[��
  - �����Ƃ��āANULL �Ƌ󕶎��͓������̂Ƃ��Ĉ����B
  - �����A���̎������� NULL ���󕶎��Ƃ��Ĉ����B
  - �����A���ŗ��� NULL �̏ꍇ�� NULL ��Ԃ��B
    `�uOracle �́A �� ���� 0�i �[���j �� ������ �� NULL �Ƃ��� ���� �� �܂� ���A �� ���� 0�i �[���j �� ������ �� �� �� �I�y�����h �� �A�� ���� �ƁA ���� ���� �� ��� ���� ��� �� �I�y�����h �ɂȂ� �܂��B ���� �� NULL �� �Ȃ� �̂́A 2 �� �� NULL ������ �� �A�� �� �� �Ƃ� �̂� �ł��B �������A ���� ���� �� Oracle Database �� ���� �� �o�[�W���� �ł� �p�� �� ��� �Ƃ� ������ �܂� ��B�v

�~�b�N. �B�l�Ɋw�� SQL �O��w�쏑 �� 2 �� �����҂ŏI��肽���Ȃ����Ȃ��� (p.144). ��������ĉj��. Kindle ��. `

- NULL ���������߂̓��ʂȊ֐�
  - COALESCE: NULLw ���w�肵���l�ɒu��������B
  - NULLIF: ����̏����ɍ��v�����ꍇ�� NULL ��Ԃ��B

### EXISTS �q�� �� �g����
