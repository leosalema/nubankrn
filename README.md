## Nubankrn

Seguindo o tutorial da RocketSeat foi feito a interface do Nubank com as animações

Neste tutorial utilizamos algumas dependências importantes:

* react-native-gesture-handler
* react-native-iphone-x-helper - para ajustar o tamnho da tela
* react-native-qrcode - para gerar os códigos 2D
* react-native-vector-icons - para os icones utlizados

Importante também na pasta android o arquivo MainActivity.java foi feito as seguintes importações: 

import com.facebook.react.ReactActivityDelegate;
import com.facebook.react.ReactRootView;
import com.swmansion.gesturehandler.react.RNGestureHandlerEnabledRootView;

e também inserimos o código abaixo. Isso é para deixar o Android com a mesma manipulação de toque que o IOS.

@Override
  protected ReactActivityDelegate createReactActivityDelegate() {
    return new ReactActivityDelegate(this, getMainComponentName()) {
        @Override
        protected ReactRootView createRootView() {
        return new RNGestureHandlerEnabledRootView(MainActivity.this);
    }
};