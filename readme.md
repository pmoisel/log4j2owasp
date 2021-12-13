# CVE-2021-44228

Short example on how to use the [dependency-check](https://github.com/jeremylong/DependencyCheck) plugin to detect CVE vulnerabilities in your dependencies.

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.owasp</groupId>
            <artifactId>dependency-check-maven</artifactId>
            <version>6.5.0</version>
            <configuration>
                <failBuildOnCVSS>8</failBuildOnCVSS>
                <suppressionFile>suppressions.xml</suppressionFile>
            </configuration>
            <executions>
                <execution>
                    <goals>
                        <goal>check</goal>
                    </goals>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

