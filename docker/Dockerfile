FROM node

WORKDIR /scratch-app

# COPY . /scratch-app

RUN git clone https://github.com/Affonso-Gui/scratch-vm
RUN git clone https://github.com/Affonso-Gui/scratch-gui

RUN (cd scratch-vm; git fetch --all; git checkout origin/fetch_extension; npm install; npm link)
RUN (cd scratch-gui; git fetch --all; git checkout origin/fetch_extension; npm install; npm link scratch-vm)

EXPOSE 8601

CMD (cd scratch-gui; npm start)