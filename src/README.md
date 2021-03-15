# Instructions
Picocrypt is written to be cross-platform, so you should be able to run the raw Python file on your OS without any issues. Picocrypt's dependencies will be automatically installed via pip, which will usually work without any issues. If Picocrypt can't automatically install dependencies, install these dependencies via pip manually: <code>argon2-cffi</code>, <code>pycryptodome</code>, and <code>reedsolo</code>.

# A note about reedsolo
Picocrypt can use the raw <code>reedsolo</code> pip package by itself, but it is very slow because it's pure Python. It is recommended to compile a Python extension (.pyd/.so) for <code>reedsolo</code>, and name it creedsolo (ie. <code>creedsolo.pyd</code> or <code>creedsolo.so</code>). Make sure to include the extension in the same directory as <code>Picocrypt.py</code>. The Windows executable already bundles <code>creedsolo.pyd</code>, but for Linux or MacOS, you'll have to build the Python extension yourself if you want better speeds. <strong>Building the extension is not necessary if you don't intend on using the Reed-Solomon feature extensively, or if you are okay with speeds ~1MB/s. Picocrypt will work just fine without the entension and just the way it is.</strong>

# External links
Here are the Github links of the dependencies of Picocrypt, if you are curious or want to audit them:
<ul>
  <li>Argon2-cffi: https://github.com/hynek/argon2-cffi</li>
  <li>Pycryptodome: https://github.com/Legrandin/pycryptodome</li>
  <li>ReedSolo: https://github.com/tomerfiliba/reedsolomon</li>
</ul>