from building import *
import os

cwd = GetCurrentDir()

path = [cwd]
src = [os.path.join(cwd, 'system_at32a403a.c')]

if rtconfig.PLATFORM in ['gcc', 'llvm-arm']:
    src += [os.path.join(cwd, 'startup', 'gcc', 'startup_at32a403a.s')]
elif rtconfig.PLATFORM in ['armcc', 'armclang']:
    src += [os.path.join(cwd, 'startup', 'mdk', 'startup_at32a403a.s')]
elif rtconfig.PLATFORM in ['iccarm']:
    src += [os.path.join(cwd, 'startup', 'iar', 'startup_at32a403a.s')]

group = DefineGroup('cmsis', src, depend = ['PKG_USING_AT32A403A_CMSIS_DRIVER'], CPPPATH = path)

Return('group')
