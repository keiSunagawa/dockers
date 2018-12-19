FROM test1

RUN curl -L -o coursier https://git.io/coursier \
        && chmod +x coursier \
        && ./coursier bootstrap \
        --java-opt -XX:+UseG1GC \
        --java-opt -XX:+UseStringDeduplication  \
        --java-opt -Xss4m \
        --java-opt -Xms1G \
        --java-opt -Xmx4G  \
        --java-opt -Dmetals.client=lsp-emacs \
        org.scalameta:metals_2.12:0.3.0 \
        -r bintray:scalacenter/releases \
        -r sonatype:releases \
        -o metals-emacs -f \
        && mv metals-emacs /usr/bin/

CMD bash
