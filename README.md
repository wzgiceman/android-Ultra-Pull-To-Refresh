#android-Ultra-Pull-To-Refresh修复横向滑动冲突问题

##修改方法
if (mDisableWhenHorizontalMove && !mPreventForHorizontal && (Math.abs(offsetX) > mPagingTouchSlop && Math.abs(offsetX) > Math.abs(offsetY))) {
    if (mPtrIndicator.isInStartPosition()) {
        mPreventForHorizontal = true;
    }
}
修改为：

if (mDisableWhenHorizontalMove && !mPreventForHorizontal && Math.abs(offsetX) > Math.abs(offsetY)) {
    if (mPtrIndicator.isInStartPosition()) {
        mPreventForHorizontal = true;
    }
}
