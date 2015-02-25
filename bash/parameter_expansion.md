#### Simple usage
```
$PARAMETER
${PARAMETER}
```

#### Indirection
```
${!PARAMETER}
```

#### Case modification
```
${PARAMETER^}
${PARAMETER^^}
${PARAMETER,}
${PARAMETER,,}
${PARAMETER~}
${PARAMETER~~}
```

#### Variable name expansion
```
${!PREFIX*}
${!PREFIX@}
```

#### Substring removal (also for filename manipulation!); * == to => a*c = abc

```
substring='a*C'
string=abcABC123abcABC123
       |----|						# shortest
	   |-------------|				# longest

${PARAMETER#PATTERN}				# strip shortest PATTERN from front of PARAMETER
${PARAMETER##PATTERN}				# strip longest PATTERN from front of PARAMETER
${PARAMETER%PATTERN}				# strip shortest PATTERN from back of PARAMETER
${PARAMETER%%PATTERN}				# strip longest PATTERN from back of PARAMETER
```

#### Search and replace
```
${PARAMETER/PATTERN/STRING}			# replace first PATTERN match with STRING
${PARAMETER//PATTERN/STRING}		# replace all PATTERN matches with STRING
${PARAMETER/PATTERN}				# ??
${PARAMETER//PATTERN}				# ??
```

#### String length
```
${#PARAMETER}
```

#### Substring expansion
```
${PARAMETER:OFFSET}
${PARAMETER:OFFSET:LENGTH}
```

#### Use a default value
```
${PARAMETER:-WORD}
```

#### Assign a default value
```
${PARAMETER:=WORD}
```

#### Use an alternate value
```
${PARAMETER:+WORD}
```

#### Display error if null or unset
```
${PARAMETER:?WORD}
```